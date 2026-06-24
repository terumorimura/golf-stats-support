# Golf Stats Privacy Policy

Effective date: June 19, 2026

Golf Stats is a scoring and statistics app for golf tournaments. This policy
explains what information the app stores and how optional sharing features work.

## Information Stored On Your Device

Golf Stats stores the tournaments, player names, rounds, holes, scores, golf
statistics, course and tee details, tee and finished times, weather details,
hole notes, review flags, followed live-score codes, your editable club bag, and
app state that you enter or create in the app. If you use the optional shot map,
it also stores the map coordinates you place for each shot and the hole, the
club, lie, stance slope, and any penalty/relief you record per shot, and the
round's course coordinate. This information is stored locally on your device
unless you choose to share or export it.

## Optional Location, Course, And Weather Helpers

Golf Stats can use your location only after you choose a location-based action.
Use Current Location requests a one-time location fix, reverse-geocodes it with
Apple MapKit, and sends the resulting state code to OpenGolfAPI to find nearby
courses. Find Course can also send the course name you type to OpenGolfAPI.

Use Current Weather requests a one-time location fix and asks Open-Meteo for the
current weather at that location. Golf Stats stores the resulting weather details
in the round if you save them, but it does not store your location coordinates.
The one-time coordinates are sent to Open-Meteo to return current weather.

## Optional Shot Map

The shot map lets you record where each shot finished on a hole. Unlike the
weather helper, the coordinates you place — by tapping the map, or by tapping My
Location to drop a pin at your current position — are stored with the round, so
the map can show where you played and the distances between shots. The map also
shows your current-location dot and can use your heading to orient an
un-mapped hole. To frame a hole you haven't pinned yet, Golf Stats looks up that
hole's tee and green from OpenStreetMap by sending the round's approximate course
location to OpenStreetMap's Overpass service over HTTPS; the result is cached on
your device. No scores, names, or identifiers are sent to OpenStreetMap. Shot-map
data is part of your round and is only shared if you share or export that round.

## Optional Plays-Like (Elevation) Distances

Each hole's shot map has an optional plays-like toggle that adjusts the displayed
distances for the rise or fall to the target. It is off by default and per hole.
When you turn it on, Golf Stats looks up the terrain elevation of the pins you
placed by sending those coordinates over HTTPS to the U.S. Geological Survey
(USGS 3DEP), Open-Meteo, and Open-Elevation — whichever first returns data — and
caches the result with the round. Only coordinates are sent; no scores, names, or
identifiers. If those services can't be reached, Golf Stats may fall back to your
device's own altitude for a pin at your current location. With the toggle on, the
adjusted distance is used on the map, in your club-distance summary, in exports,
and (for a shared round) for followers.

## Apple Watch Companion

Golf Stats includes an optional Apple Watch app for scoring a round from your
wrist. Your iPhone holds your data; the watch and iPhone exchange the current
round's scores and your tapped actions directly with each other over Apple's
WatchConnectivity. The watch app can use your location only after you tap Drop
Shot or Set Hole, to record where a shot was struck or where the hole is (stored
with the round, the same as the shot map). While a round is connected, the watch
keeps itself in the foreground (so raising your wrist returns to the app) using a
standard watchOS runtime session; Golf Stats does **not** use Apple HealthKit and
reads no health or fitness data. You can decline the location prompt and still
move between holes; only shot/hole-location capture is skipped.

## Live Score Sharing

If you choose Share Live Scores, Golf Stats publishes a live scorecard to
Apple's public CloudKit database. The live scorecard can include the tournament
name, optional player name, dates, round names, course and tee, tee time,
finished time, weather, hole numbers, distance, par, handicap index, score,
fairway results, approach-for-GIR, greens in regulation, first-putt distance,
putts, penalties, hole notes, review flags, shot-map coordinates (when a shared
hole has a shot map), current round/hole, update time, and a random share code.

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
tournament file. When a hole has a shot map, the scorecard PDF includes per-hole
shot-map images (your placed pins drawn over Apple Maps satellite imagery). These
exports are created only when you choose to share or export them. When you use the iOS share sheet, the destination you choose is
responsible for how it handles the exported file.

## Tracking, Ads, And Analytics

Golf Stats does not track you across apps or websites. Golf Stats does not
include advertising, advertising SDKs, third-party analytics SDKs, or data
broker integrations.

## iCloud, Weather, MapKit, And Course Lookup

Live score sharing uses Apple's CloudKit service. Apple's handling of iCloud and
CloudKit data is governed by Apple's privacy practices. Location-based weather
uses Open-Meteo over HTTPS. Reverse geocoding uses Apple's MapKit service.
Course lookup uses OpenGolfAPI. The shot map uses Apple's MapKit for the
satellite map and OpenStreetMap's Overpass service for hole tee/green geometry.
The optional plays-like distance feature looks up terrain elevation from USGS
3DEP, Open-Meteo, and Open-Elevation over HTTPS, sending only pin coordinates.

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
