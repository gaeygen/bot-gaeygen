# splinterlands-bot

## index.js 
run `npm start` 

to start BOT login routine. username and password needs to be specified. **currently working until cards selection**.


## battleGet.js 
run `node battleGet.js` 

to generate the file 'playerName.json' with the history of the battles and print the list of distinct players.

input data for future model:

- *mana_cap*: the total mana that can be selected
- *ruleset*: rules applied for the match (to be explored)
- *inactive*: type of monster card that are not available for the match. important for the summoner selection (first card) 
- *details_team(1 and 2)*:
    - *summoner*: main card to be selected. important info for the model are _"card_detail_id"_ and _"level"_.
    _Example:` 
        "summoner":{ 
         "uid":"starter-167-2UoZi",
         "xp":1,
         "gold":false,
         "card_detail_id":167,
         "level":1,
         "edition":4,
         "state":{  }`_
    
    - *monsters*: array of team cards. Important variables for the models are _"card_detail_id"_, _"abilites"_ (array), and _"level"_.
        _Example:` 
              "monsters":[ 
                { 
                    "uid":"starter-162-bZwj2",
                    "xp":1,
                    "gold":false,
                    "card_detail_id":162,
                    "level":1,
                    "edition":4,
                    "state":{  },
                    "abilities":[ 
                    "Shield"
                    ]
                },
                { 
                    "uid":"starter-160-zCoGb",
                    "xp":1,
                    "gold":false,
                    "card_detail_id":160,
                    "level":1,
                    "edition":4,
                    "state":{  },
                    "abilities":[
                    ]
                }
            ]`_
    
