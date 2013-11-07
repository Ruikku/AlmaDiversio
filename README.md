AlmaDiversio
============
# Task in brief

Create a small app for Windows Phone, iOS or Android (choose the platform you like and know the best) based on the layout provided with the task with the data from Telkku.com API.

## App Requirements:
* Fetch channel/program data via the Telkku API
* Show a list of programs from "Yle TV1"-channel (as defined in Layout-ChannelView.png)
* When user taps a program item on the list, they will be shown detailed information: time, name, picture (if available) and description about the program (as defined in Layout-ProgramView.png)
* User should be able to close the detailed program view (Layout-ProgramView.png) and be shown the channel view (Layout-ChannelView.png) again by either:
** Tapping the "X"-button on the top right corner
** Tapping the transparent black vertical area on the left side of program detail view
** Swiping from left to right

## Platform Requirements
* Create the app on the platform of your choice (Windows Phone, iOS, Android) with the technology of your choice
* Depending on your platform choices, the app should work with:
** Android 4.x
** iOS 6.x
** Windows Phone 8.x
* To keep this exercise reasonable, the app only needs to work on "smartphone screen sizes" (basically 5 inch screens and below). No need to make it work with tablets etc.

## Deliverables
* Provide the finished app as and installable package with instructions
* Provide your source codes as a zipped Git-repo


## The finished app will be evaluated by the following principles:
* Functional app
* Clean project structure
* Clean and commented code
* Unit tests and integration tests (where applicable)
* Readability of the code
* Smoothness/responsiveness of the user interface


## API calls

The API is documented at [api.telkku.com](http://api.telkku.com).

The parts that are of interest for this task are The Envelope, Authorizing Access To The API and Programs API.

### API-key

X-telkku-app-key

3e6e6758ff3b6823b0134604a8b0acc3d022af3a26b53188e1dbe29fc84a1569

### Quick start

For the purposes of this task, you'll only need to make two API calls (or one, depends on how you implement the app):

**Fetch a list of programs for YLE 1**

```
GET http://api.telkku.com/v1/channels/1/programs?queryRangeStart=2013-04-17T00:00:00.000+03:00&queryRangeEnd=2013-04-17T23:59:00.000+03:00
```

**Fetch data for single program**

```
GET http://api.telkku.com/v1/programs/[:id]
```

For easy testing and examination of the API, we recommend the Postman extension for Chrome.
