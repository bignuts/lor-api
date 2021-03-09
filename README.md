# lor-api - Legends of Runeterra dataset repository

The repository contains all the available dataset published from https://developer.riotgames.com/docs/lor since 1.0.0 version of the game.

## How to use:

There are two ways to use the dataset, preferred one is to fetch data API style with [jsDelivr](https://www.jsdelivr.com/), or just clone the repository.

### jsDelivr:

Make GET request to following links and options.
https://cdn.jsdelivr.net/gh/bignuts/lor-api@[branch]/[language-code]/[resource]

EXAMPLE

**[resource]**
| Path | Resource |
| ------------- |:-------------:|
| cards.json | All cards |
| cards/[cardCode].json | Single card |
| keywords.json | All keywords |
| keywords/[nameRef].json | Single keyword |
| rarities.json | All rarities |
| rarities/[nameRef].json | Single rarity |
| regions.json | All regions |
| regions/[nameRef].json | Single region |
| spellSpeeds.json | All spellSpeeds |
| spellSpeeds/[nameRef].json | Single spellSpeed |
| vocabTerms.json | All vocabTerms |
| vocabTerms/[nameRef].json | Single vocabTerm |

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
  "01SI053": {...},
  ...
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

Fetching Regions, Chinese language, 1.0.0 release -> https://cdn.jsdelivr.net/gh/bignuts/lor-api@1_0_0/v1/zh_tw/regions.json

```json
{
  "Noxus": {
    "abbreviation": "NX",
    "iconAbsolutePath": "http://dd.b.pvp.net/1_0_0/core/zh_tw/img/regions/icon-noxus.png",
    "name": "諾克薩斯",
    "nameRef": "Noxus"
  },
  "Demacia": {
    "abbreviation": "DE",
    "iconAbsolutePath": "http://dd.b.pvp.net/1_0_0/core/zh_tw/img/regions/icon-demacia.png",
    "name": "蒂瑪西亞",
    "nameRef": "Demacia"
  },
  "Freljord": {
    "abbreviation": "FR",
    "iconAbsolutePath": "http://dd.b.pvp.net/1_0_0/core/zh_tw/img/regions/icon-freljord.png",
    "name": "弗雷爾卓德",
    "nameRef": "Freljord"
  },
  "ShadowIsles": {
    "abbreviation": "SI",
    "iconAbsolutePath": "http://dd.b.pvp.net/1_0_0/core/zh_tw/img/regions/icon-shadowisles.png",
    "name": "闇影島",
    "nameRef": "ShadowIsles"
  },
  "Ionia": {
    "abbreviation": "IO",
    "iconAbsolutePath": "http://dd.b.pvp.net/1_0_0/core/zh_tw/img/regions/icon-ionia.png",
    "name": "愛歐尼亞",
    "nameRef": "Ionia"
  },
  "Bilgewater": {
    "abbreviation": "BW",
    "iconAbsolutePath": "http://dd.b.pvp.net/1_0_0/core/zh_tw/img/regions/icon-bilgewater.png",
    "name": "比爾吉沃特",
    "nameRef": "Bilgewater"
  },
  "PiltoverZaun": {
    "abbreviation": "PZ",
    "iconAbsolutePath": "http://dd.b.pvp.net/1_0_0/core/zh_tw/img/regions/icon-piltoverzaun.png",
    "name": "皮爾托福 & 佐恩",
    "nameRef": "PiltoverZaun"
  }
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
