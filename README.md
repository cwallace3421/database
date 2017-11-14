# database
JSON Database of all the game and homebrew entries. Propose here additions, improvements and fixes, every change propagates to Homebrew Hub.

## How to propose changes

Clone this repository locally

```
git clone https://github.com/dmg01/database
```

The `games.json` file is an array of objects, each one representing a game entry.
```json

[
    Game1,
    Game2,
    Game3,
    [...]
]

```

Each Game is an object respecting the following structure

| Property Name | Description                                                          | Possible values                                         |
|---------------|----------------------------------------------------------------------|---------------------------------------------------------|
| title         | The complete name, including spacing.                                | String                                                  |
| permalink     | A short identificative name that will be the in the URL              | String, Only letters, underscores, dashes and numbers   |
| license       | Identifier of the license under whose terms the software is released | [Identifier](https://spdx.org/licenses/) of the license |
| developer     | GitHub username of the developer                                     | String                                                  |
| repository    | Repository or URL where the source can be found                      | String                                                  |
| platform      | Target console                                                       | String, `GB` or `GBC`                                   |
| typetag       | The type of the software                                             | String, `game`, `homebrew` or `demo`                    |
| tags          | A list of the categories representing the entry                      | Array of String, [existing categories]()                |

E.g., this is a valid entry:

```json
    {
        "title": "uCity",
        "permalink": "ucity",
        "license": "GPLv3",
        "developer": "AntonioND",
        "repository": "https://github.com/AntonioND/ucity",
        "platform": "GBC",
        "typetag": "game",
        "tags": [ "Open Source", "RPG", "Adventure" ]
    }
```


If you want to add a game, simply add - at the **end** of the array - an object with the details of your game, complying with the described schema.

You're welcome to edit, correct or improve existing entries.

### Files

