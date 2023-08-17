base url: https://sportapi.mlssoccer.com/
| [SCHEDULE ENDPOINTS](#schedule-endpoints) |                                                    |
| ----------------------------------------- | -------------------------------------------------- |
| [Schedule](#schedule)                     | see [modifiers](#schedule-modifiers) for varietals |
<!-- | [Seasons](#seasons)                       | ties? Divisions? Olympics? etc                     | -->

Game Schedule:

If no date is specified, every mls match ever is returned
?culture=en-us








<!-- [back to top](#endpoint-tables) -->
# Schedule endpoints

## Schedule

`GET https://sportapi.mlssoccer.com/api/matches` Returns a list of data about the schedule for a specified date range. If no date range is specified, every mls match ever is returned.

<!-- >Note: If no date is specified, every mls match ever is returned -->



#### Schedule Modifiers

<!-- `?expand=schedule.broadcasts` Shows the broadcasts of the game

`?expand=schedule.linescore` Linescore for completed games

`?expand=schedule.ticket` Provides the different places to buy tickets for the upcoming games -->

`?clubOptaId=14880` Limit results to a specific team(s). 

`?excludeSecondaryTeams=True` Exclude clubs secondary teams from the results

<!-- `?date=2018-01-09` Single defined date for the search -->

`?dateFrom=2023-08-16` Start date for the search

`?dateTo=2023-08-17` End date for the search

`?seasonOptaId=2023` Returns all games from specified season

`?matchType=Regular` Restricts results to only regular season games. Not quite sure how to use this when you can use `?competition=98`

`?competition=98` Restricts results to only MLS regular season games. 


#### Examples
</details>

`GET https://sportapi.mlssoccer.com/api/matches?clubOptaId=14880&dateFrom=2023-08-15&dateTo=2023-08-15` Returns Inter Miami games for August 15, 2023.

<details>
  <summary>click for example</summary>

```json
[
  {
    "optaId": 2399563,
    "slug": "phivsmia-08-15-2023",
    "leagueMatchTitle": "",
    "home": {
      "optaId": 5513,
      "fullName": "Philadelphia Union",
      "slug": "philadelphia-union",
      "shortName": "Philadelphia",
      "abbreviation": "PHI",
      "backgroundColor": "#041c2c",
      "logoBWSlug": "webcomp_5033df5a-f2dd-4d54-a023-970ab81ec759",
      "logoColorSlug": "webcomp_b69fdee0-e31b-4e72-b095-d8ae3e277b98",
      "logoColorUrl": "https://images.mlssoccer.com/image/upload/{formatInstructions}/v1614970756/assets/logos/5513-philadelphia-logo_ea33hb.png",
      "crestColorSlug": "webcomp_d0a30390-f72f-4a8d-aca1-520c6dcc3b1b"
    },
    "away": {
      "optaId": 14880,
      "fullName": "Inter Miami CF",
      "slug": "inter-miami-cf",
      "shortName": "Miami",
      "abbreviation": "MIA",
      "backgroundColor": "#212322",
      "logoBWSlug": "webcomp_67e7f2c7-e631-4355-950c-4bc3c10bdb21",
      "logoColorSlug": "webcomp_15509514-e261-43f0-9b44-284b34236321",
      "logoColorUrl": "https://images.mlssoccer.com/image/upload/{formatInstructions}/v1614970761/assets/logos/14880-miami-logo_m0n453.png",
      "crestColorSlug": "webcomp_235c0a61-f516-4036-b693-ed09a21ad154"
    },
    "venue": {
      "venueOptaId": "6548",
      "backgroundImageSlug": "",
      "name": "Subaru Park",
      "city": "Chester, PA"
    },
    "season": {
      "slug": "leagues-cup-season-2023-2024",
      "optaId": 2023,
      "competitionId": 1209,
      "name": "Season 2023/2024"
    },
    "competition": {
      "optaId": 1209,
      "name": "Leagues Cup",
      "slug": "leagues-cup",
      "shortName": "Leagues Cup",
      "matchType": "",
      "logoLight": {
        "slug": ""
      },
      "logoDark": {
        "slug": ""
      },
      "blockHeaderName": "",
      "mgmId": "0",
      "playerHeadshotThumbnailField": ""
    },
    "broadcasters": [
      {
        "broadcasterTypeLabel": "",
        "broadcasterName": "Apple TV - MLS Season Pass",
        "broadcasterStreamingURL": "https://tv.apple.com/channel/tvs.sbd.7000",
        "broadcasterType": "International Streaming"
      }
    ],
    "sponsorImage": {},
    "matchDate": "2023-08-15T23:00:00.0000000Z",
    "firstPartyTickets": {
      "displayText": "Buy Tickets",
      "accessibleText": "Buy Tickets",
      "url": "https://philadelphiaunion.evenue.net/cgi-bin/ncommerce3/SEGetEventInfo?ticketCode=GS:GLOBAL-UNION:OSE23:LC6:&linkID=global-union&RDAT=&RSRC=&dataAccId=165&locale=en_US&siteId=ev_global-union",
      "openInNewTab": true,
      "isVisible": false
    },
    "tags": [],
    "homeClubBroadcasters": [],
    "awayClubBroadcasters": [],
    "clubBroadcasters": [],
    "isTimeTbd": false,
    "mgmId": "",
    "appleStreamURL": "https://tv.apple.com/sporting-event/philadelphia-union-vs-inter-miami-cf/umc.cse.3b4y5i3dvswnc2z0subsw9t8b?itsct=s_mls_partner_gp&itscg=80103",
    "appleSubscriptionTier": "",
    "appleAdvertisementCategory": "",
    "roundName": "Semi-Finals",
    "roundNumber": 5,
    "roundGroup": "",
    "matchDay": "7",
    "delayedMatch": false
  }
]
```

<br /></details>

[back to top](#endpoint-tables)
