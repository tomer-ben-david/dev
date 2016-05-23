# Push notification

1. The whole point of push notification is that android already holds an open connection which consumes low power (no data) so it already has an open connection to its servers so we are reusing that only open connection for push notifications! if you do pull you use X40 power consumption.
1. **authentication token** - your applicaiton server should send an http request to google with your credentials to get an authentication token.
1. **token** Identifies your specific mobile phone and application so we can send the push notification specifically to the app on your phone.
2. So that your `application server` will know your mobile you need to send the `token` you mobile phone app generated while communicating with google servers and send it to your `application server` such that he can identify your app on your phone.
3. Security usually you only ask `google` to send push notification to your app without real data and the app itself would fetch the actual data from your `application server` so google is not aware of the actual data in push notification.
1. [push notification tutorial](http://my.safaribooksonline.com/video/programming/android/9781449322205/platform-development-pushing-bits-from-the-cloud-android-and-push-notification/oreillyvideos935635?query=((push+notification))#snippet)
