# lor-api - Legends of Runeterra assets repository

The repository contains all the available assets published from https://developer.riotgames.com/docs/lor since 1.0.0 version of the game.

## How to use:

There are two ways to use the assets, preferred one is to fetch data API style with [jsDelivr](https://www.jsdelivr.com/), or just clone the repository.

### jsDelivr:

Make GET request to following links and options.
https://cdn.jsdelivr.net/gh/bignuts/lor-api@[branch]/[language-code]/[resource]

EXAMPLE

**[resource]**
| Path | Resource |
| ------------- |:-------------:|
| cards.json | All cards |
| cards/[cardCode].json | Single card |

**[@branch]**
| Branch | Game Version |
| ------------- |:-------------:|
| master | latest |
| 1_0_0 | 1.0.0 |

**[language-code]**
| Language Code | Language |
| ------------- |:--------:|
| de_de | German (Germany) |
| en_us | English (United States) |
| es_es | Spanish (Spain) |
| es_mx | Spanish (Mexico) |
| fr_fr | French (France) |
| it_it | Italian (Italy) |
| ja_jp | Japanese (Japan) |
| ko_kr | Korean (Korea) |
| pl_pl | Polish (Poland) |
| pt_br | Portuguese (Brazil) |
| th_th |Thai (Thailand) |
| tr_tr |Turkish (Turkey) |
| ru_ru | Russian (Russia) |
| zh_tw | Chinese (Taiwan) |

##### Examples:

Fetching all cards, Russian language, latest release -> https://cdn.jsdelivr.net/gh/bignuts/lor-api@master/v1/ru_ru/cards.json

```json
{
  "01NX038": {...},
  "01SI033": {...},
  "01SI053": {...}
}
```

Fetching Jubilant Poro, English language, 1.0.0 release -> https://cdn.jsdelivr.net/gh/bignuts/lor-api@1_0_0/v1/en_us/cards/01FR008T1.json

```json
{
  "associatedCards": [],
  "associatedCardRefs": [],
  "assets": [
    {
      "gameAbsolutePath": "http://dd.b.pvp.net/1_0_0/set1/en_us/img/cards/01FR008T1.png",
      "fullAbsolutePath": "http://dd.b.pvp.net/1_0_0/set1/en_us/img/cards/01FR008T1-full.png"
    }
  ],
  "region": "Freljord",
  "regionRef": "Freljord",
  "attack": 1,
  "cost": 1,
  "health": 1,
  "description": "When I'm summoned, create in hand another random 1 cost Poro from any region.",
  "descriptionRaw": "When I'm summoned, create in hand another random 1 cost Poro from any region.",
  "levelupDescription": "",
  "levelupDescriptionRaw": "",
  "flavorText": "\"Oho, there's a good lad! Even the coldest winter melts into spring.\" - Poro Herder",
  "artistName": "SIXMOREVODKA",
  "name": "Jubilant Poro",
  "cardCode": "01FR008T1",
  "keywords": [],
  "keywordRefs": [],
  "spellSpeed": "",
  "spellSpeedRef": "",
  "rarity": "None",
  "rarityRef": "None",
  "subtype": "PORO",
  "subtypes": ["PORO"],
  "supertype": "",
  "type": "Unit",
  "collectible": false
}
```

Fetching Jinx, Chinese language, 1.0.0 release -> https://cdn.jsdelivr.net/gh/bignuts/lor-api@1_0_0/v1/zh_tw/cards/01PZ040.json

```json
{
  "associatedCards": [],
  "associatedCardRefs": ["01PZ040T2", "01PZ040T1", "01PZ040T3"],
  "assets": [
    {
      "gameAbsolutePath": "http://dd.b.pvp.net/1_0_0/set1/zh_tw/img/cards/01PZ040.png",
      "fullAbsolutePath": "http://dd.b.pvp.net/1_0_0/set1/zh_tw/img/cards/01PZ040-full.png"
    }
  ],
  "region": "皮爾托福 & 佐恩",
  "regionRef": "PiltoverZaun",
  "attack": 4,
  "cost": 4,
  "health": 3,
  "description": "",
  "descriptionRaw": "",
  "levelupDescription": "此牌在場上時我方用盡手牌。",
  "levelupDescriptionRaw": "此牌在場上時我方用盡手牌。",
  "flavorText": "「怎麼啦，惡鯊？」\n「我好擔心你喔，吉茵珂絲！每次你無聊就會想要...」\n「想要來個大轟炸！惡鯊，這真是好主意！」",
  "artistName": "SIXMOREVODKA",
  "name": "吉茵珂絲",
  "cardCode": "01PZ040",
  "keywords": ["快速攻擊"],
  "keywordRefs": ["QuickStrike"],
  "spellSpeed": "",
  "spellSpeedRef": "",
  "rarity": "英雄",
  "rarityRef": "Champion",
  "subtype": "",
  "subtypes": [],
  "supertype": "英雄",
  "type": "單位",
  "collectible": true
}
```

### git clone:

Open terminal and run command below.

```sh
git clone https://github.com/bignuts/lor-api.git
```

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
lor-api was created under Riot Games' "Legal Jibber Jabber" policy using assets owned by Riot Games. Riot Games does not endorse or sponsor this project.
