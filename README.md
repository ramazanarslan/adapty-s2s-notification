## App Store In-App Purchase Event Notification Sender 🔔
This repo monitors [**App Store Server to Server Version 2**](https://developer.apple.com/documentation/appstoreservernotifications) events for **in-app purchases** and notifies you on **Slack or Discord** in a convenient format. Ideal for individual developers with low purchase requests.

![image](https://github.com/ramazanarslan/ios-raw-events-notification/assets/31334024/2a4d325a-9211-4bbf-acfd-6fb664bc4cd3)



![image](https://github.com/ramazanarslan/ios-raw-events-notification/assets/31334024/947f8dc0-dbce-4ddc-abde-56f768f266d3)



# Integration

![image](https://github.com/ramazanarslan/ios-raw-events-notification/assets/31334024/39f9fbb2-5a9c-4e1f-9432-56d0c8e6f714)


1. Get Incoming Webhook URL 🔗 from Slack or Discord
2. Create a new Google Cloud Function (2 Million request monthly free usage)
3. Change `WEBHOOK_URL` constant in code
4. Upload this code to Cloud Function
5. Copy Cloud Function URL 🔗  and paste to Adapty / RevenuCat Panel
6. Done ✅

## Deploying our code to Google Cloud Function and getting the required URL

## Forwarding  Apple S2S events

### 1. Using [Adapty.io](https://adapty.io/)
<img width="138" alt="image" src="https://github.com/ramazanarslan/ios-raw-events-notification/assets/31334024/614b8c90-d497-4189-9640-677a0fb1497e">

1. Open [Adapty.io](https://app.adapty.io/)
2. Navigate to **App settings > Apps** in the Adapty dashboard.
3. Click to the **iOS SDK** section, scroll to **App Store server notifications**.
4. Enter your the URL to **URL for forwarding raw Apple events**
5. Click **Save** in the bottom left corner.

![image](https://github.com/ramazanarslan/ios-raw-events-notification/assets/31334024/fab237b4-ef34-4db7-8626-ac4fe0be902f)





[🔗 Adapty documentation link](https://docs.adapty.io/docs/app-store-server-notifications#raw-events-forwarding)


---------
### 2. Using [RevenueCat.com](https://www.revenuecat.com)
<img width="144" alt="image" src="https://github.com/ramazanarslan/ios-raw-events-notification/assets/31334024/6e20bff6-2d26-4afa-ae18-3a4fba192825">

1. Open [RevenueCat](https://www.revenuecat.com/)
2. Navigate to your iOS app under **Project settings > Apps** in the RevenueCat dashboard.
3. Scroll to the **Apple Server to Server notification settings** section, and enter your the URL in **Apple Server Notification Forwarding URL**.
4. Click **Save Changes** in the top right corner.

![image](https://github.com/ramazanarslan/ios-raw-events-notification/assets/31334024/be1d97e3-ee15-4c06-874b-61cef9249872)



[🔗 RevenueCat documentation link](https://www.revenuecat.com/docs/platform-resources/server-notifications/apple-server-notifications#option-1-recommended-setting-up-revenuecat-to-forward-apple-notifications-to-your-server)

---------
### 3. Using an internal solution
If you are using an internal solution, your own backend url is probably added here. Therefore, you can prepare an endpoint for your own backend and give it to the Google Cloud function we prepared as the raw event arrives.

*App Store Connect -> General -> App Information -> App Store Server Notifications*

![image](https://github.com/ramazanarslan/ios-raw-events-notification/assets/31334024/63520a2a-4437-4be8-afad-ea78793772aa)



### Why Google Cloud Function ?
Because it has 2 Million request monthly free usage rights. This may be sufficient, especially for individual developers.
https://cloud.google.com/functions/pricing 


