# Golf Stats Privacy Policy

Effective date: June 10, 2026

Golf Stats is a scoring and statistics app for golf tournaments. This policy
explains what information the app stores and how optional sharing features work.

## Information Stored On Your Device

Golf Stats stores the tournaments, player names, rounds, holes, scores, golf
statistics, course and tee details, tee and finished times, weather details,
hole notes, review flags, followed live-score codes, and app state that you enter or create
in the app. This information is stored locally on your device unless you choose
to share or export it.

## Optional Location, Course, And Weather Helpers

Golf Stats can use your location only after you choose a location-based action.
Use Current Location requests a one-time location fix, reverse-geocodes it with
Apple MapKit, and sends the resulting state code to opengolfapi to find nearby
courses. Find Course can also send the course name you type to opengolfapi.

Use Current Weather requests a one-time location fix and asks Open-Meteo for the
current weather at that location. Golf Stats stores the resulting weather details
in the round if you save them, but it does not store your location coordinates.
The one-time coordinates are sent to Open-Meteo to return current weather.

## Live Score Sharing

If you choose Share Live Scores, Golf Stats publishes a live scorecard to
Apple's public CloudKit database. The live scorecard can include the tournament
name, optional player name, dates, round names, course and tee, tee time,
finished time, weather, hole numbers, distance, par, handicap index, score,
fairway results, approach-for-GIR, greens in regulation, first-putt distance,
putts, penalties, hole notes, review flags, current round/hole, update time,
and a random share code.

People with the share code or `golfstats://live/CODE` link can view the live
scorecard while sharing is on. When you stop sharing, Golf Stats attempts to
remove the live CloudKit record.

## Live-Round Notifications

If you follow a live round, you can optionally turn on notifications to be
alerted as that player updates their round. Notifications are delivered through
Apple's CloudKit and Apple Push Notification service, and are sent only when you
grant the standard iOS notification permission. Your notification preferences
(whether notifications are on and how often) are stored
locally on your device. Golf Stats does not send your notification preferences
or device token to any server other than Apple's.

## Exports And Sharing

Golf Stats can create a scorecard PDF, spreadsheet export, or `.golfstats`
tournament file. These exports are created only when you choose to share or
export them. When you use the iOS share sheet, the destination you choose is
responsible for how it handles the exported file.

## Tracking, Ads, And Analytics

Golf Stats does not track you across apps or websites. Golf Stats does not
include advertising, advertising SDKs, third-party analytics SDKs, or data
broker integrations.

## iCloud, Weather, MapKit, And Course Lookup

Live score sharing uses Apple's CloudKit service. Apple's handling of iCloud and
CloudKit data is governed by Apple's privacy practices. Location-based weather
uses Open-Meteo over HTTPS. Reverse geocoding uses Apple's MapKit service.
Course lookup uses opengolfapi.

## Children's Privacy

Golf Stats is a general-audience sports utility and does not knowingly collect
personal information from children for advertising or tracking.

## Deleting Your Data

You can delete tournaments in the app. You can stop live sharing to remove the
active live scorecard from CloudKit; deleting a tournament that is being shared
live, or clearing all data, also stops sharing and attempts to remove its live
scorecard. You can also delete the app from your device
to remove local app data from that device, subject to normal iOS and iCloud
backup behavior.

## Contact

For privacy questions, open an issue at:

<https://github.com/terumorimura/golf-stats-support/issues>
