# PWNY (/ˈpōnē/) 

**PWNY** is an iOS app to interface with the [HaveIBeenPwned (HIBP) API](https://haveibeenpwned.com/API/v3) 

With PWNY, you can easily find out if one of your passwords or usernames has leaked in a known data breach. Early knowledge is crucial to quickly locking your accounts back down and mitigating damage potential.

If you want to see pretty pictures and learn about how it was made, read on. If you just want to play with the code, hop right in 😊. 

PWNY is built mostly as a practice exercise, but the app is fully functional if an API key is provided. It supports the following features:

- Check an e-mail or username against the database of breaches
- Check an e-mail against the database of pastes
- Check a password against the database of leaked passwords
- View all breaches registered in the HIBP database
- View detailed info about a specific breach
- Get tips about why this matters and why you should care about your password security
- Native dark mode support (ok, fine, that comes for free with modern iOS dev... but still)

## Screenshots

Home Screen         |  Expanded Home 1 | Expanded Home 2 | All Breaches
:-------------------------:|:-------------------------:|:-------------------------:|:------------------------:
![Pwny Home Screen](https://tarrouye.net/ios/pwny/assets/main_screen.png)  |  ![Pwny Expanded Home](https://tarrouye.net/ios/pwny/assets/main_expanded_1.png) | ![Pwny Expanded Home 2](https://tarrouye.net/ios/pwny/assets/main_expanded_2.png) | ![Pwny All Breaches View](https://tarrouye.net/ios/pwny/assets/all_breaches.png)




Check Account against Breaches |  Check Account against Pastes | Check Password | Breach Details
:-------------------------:|:-------------------------:|:-------------------------:|:---------------:
![Pwny Breach Check Results](https://tarrouye.net/ios/pwny/assets/breach_check_results.png)  |  ![Pwny Pastes Check Results](https://tarrouye.net/ios/pwny/assets/paste_check_result.png) | ![Pwny Password Check Results](https://tarrouye.net/ios/pwny/assets/password_check_result.png) | ![Pwny Breach Details](https://tarrouye.net/ios/pwny/assets/breach_details.png)


## Tech stack

PWNY is built with Swift 5 and SwiftUI 2.0

## Dependencies

The only dependency is the incredible [Atributika](https://github.com/psharanda/Atributika), which provides "an easy and painless way to build NSAttributedString."

The Podfile is included in the repository so all you should need to do is 

> cd /path/to/repo
>
> pod install

The only other potential 'gotcha' is that without a paid API key, only viewing all breaches will work. 

## Fun / useful parts

 - `URLImage`, a SwiftUI `View` that takes a `URL` and placeholder `View`. It asynchronously loads the image from the URL and displays the placeholder view while waiting. 
 - `BackgroundBlurView`, a SwiftUI `View` to be used in .background() modifier or under views to provide the native frosted glass effect. Simply wraps a `UIVisualEffectView` with `UIBlurEffect` thin style.
 - `HIBPQueryManager`, or HaveIBeenPwnedQueryManager, which handles fetching data from the HIBP API. Note that to make full use of this you will need an API Key stored in a global variable somewhere called `API_KEY`. 
 
## Feedback
If you have any feedback about the code or want to contribute, please open a Pull Request, an Issue, or shoot me an e-mail. This is one of my first SwiftUI applications and I'm always open to constructive criticism. 

## License
You may take any of the code found within this repository and do whatever you wish with it. Take the app, plug in your own API key, and sell it on the App Store as is, for all I care 😊 

When the opportunity presents itself, please give back to the community! 
