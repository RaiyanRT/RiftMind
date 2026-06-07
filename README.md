# RiftMind
League of Legends Habit Trainer

## About

As a League player I can sometimes go into autopilot and hard focus on my lane or whatever I'm doing right then. As a ranked player that isn't a good habit, especially when you're trying to climb. To get better I need to build habits into myself so I'm paying attention to the broader game state. This is something most players struggle with when climbing, building these habits into their mindset.

To tackle this, RiftMind is a fully customisable League notification system where players create their own timed reminders that fire while they're in game. As a support main I'd set a reminder every minute asking "where is the Jungler" so I'm forced to look at the map and think about where he is. Or in mid when you're a melee champ into a ranged one, a ping for when the first honey fruit spawns so you know you can take a bad trade for cs and heal it back.

Each reminder works on a simple start, step, stop system. You set when it first fires, how often it repeats, and when it stops, so jungle tracking might start at 0:30, repeat every 60 seconds and stop at 14:30. Players can make as many reminders as they want based on what helps them, and set separate ones depending on the role they play. There will also be presets based on role to get people started. The reminders created will all be stored on the user's local machine, so there is no personal information or storage problems.

## Technical approach

RiftMind reads live game state via Overwolf's Game Events Provider from the local League client. It does not call Riot Games' web APIs.

## MVP scope

**App behaviour**
- Opens automatically when the League client launches
- Reminders configured in the client lobby before queuing into a game

**Habit reminders**
- Custom message field (emoji supported, with a character limit)
- Start: when the reminder first fires (e.g. 0:30)
- Step: how often it repeats (e.g. every 60 seconds)
- Stop: when it stops firing (e.g. 14:30)
- Auto-dismiss duration (user configurable)
- Toggle on/off per reminder

**Notification design**
- Sound ping plus text popup
- Draggable anywhere on screen
- Auto-dismisses

## Roadmap (post-MVP)

**Objective reminders**: Dragon, Baron, Rift Herald, Void Grubs. Alert fires a customisable number of seconds before spawn, using the same notification system as habit reminders.

## Status

Currently in the application phase and waiting for approval. 
