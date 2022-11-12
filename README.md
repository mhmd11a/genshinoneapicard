<p align="center">
 <img src="img/banner.jpg" alt="Баннер"/>
</p>

# EnkaNetworkCard
Wrapper for [EnkaNetwork.py](https://github.com/mrwan200/EnkaNetwork.py) creation to create character cards in Python.

## Navigation
* Installation
* Dependencies
* Launch
* Description of arguments
* Sample Results

## Installation:

```
pip install enkanetworkcard
```
Or you can copy the given repository.

### Dependencies:
  Dependencies that must be installed for the library to work:
  * googletrans-3.1.0a0
  * Pillow
  * requests
  * io
  * math
  * threading
  * datetime
  * random
  * enkanetwork
  * logging

## Launch:
``` python
from enkanetworkcard import encbanner

ENC = encbanner.EnkaGenshinGeneration() 

result = ENC.start(uids = 724281429)

print(result)

```

## Description of arguments:
``` 
--|EnkaGenshinGeneration - Main class.
----|lang - Takes one value to define the language. Supported languages are listed below in the documentation. The default is Russian.
------|Values: str
--------|Example str: EnkaGenshinGeneration(lang = "en")

----|img - If you want to use your image on the card, then pass this argument.
------|Values: str, list, PIL.ImageFile
--------|str: image link or the path to the file.
--------|PIL.ImageFile: Image opened with Image.open()
--------|list: image link, the path to the file or PIL.ImageFile
----------|Example str - the path to the file: EnkaGenshinGeneration(img = "img.png")
----------|Example str - image link: EnkaGenshinGeneration(img = "https//...image.png")
----------|Example PIL.ImageFile: EnkaGenshinGeneration(img = Image.open("img.png"))
----------|Example list: EnkaGenshinGeneration(img = [Image.open("img.png"), "img.png", "https//...image.png"]) #list only works with the argument: random.

----|charterImg - Give each character a custom image.
------|Values: dict
--------|dict: can take all values from the img argument except list.
----------|Example dict: EnkaGenshinGeneration(charterImg = {"Klee": Image.open("img.png"), "Albedo": "img.png", "Xiao": "https//...image.png"})

----|name - Needed if you want to get certain characters.
------|Values: str
----------|Example str - One character: EnkaGenshinGeneration(name = "Klee")
----------|Example str - Two or more characters: EnkaGenshinGeneration(name = "Klee, Albedo, ...")

----|adapt - Adapt background to custom image.
------|Values: bool
----------|Example bool: EnkaGenshinGeneration(img = "img.png", adapt = True)

----|randomImg - Random selection of custom images from the list.
------|Values: bool
----------|Example bool: EnkaGenshinGeneration(img = [Image.open("img.png"), "img.png"], randomImg = True) #If img is not a list, then randomImg is ignored.

----|hide - Hide the UID on the character card.
------|Values: bool
----------|Example bool: EnkaGenshinGeneration(hide = True)

----|dowload - Will return ready images for further work with them. (If not specified, then the finished results will be saved in the directory of the executable file in the folder: EnkaImg)
------|Values: bool
----------|Example bool: EnkaGenshinGeneration(dowload = True)

--|start - EnkaGenshinGeneration class method
----|uids - Game UID in the game Genshin Impact. (Can take multiple values.)
------|Values: int, str
----------|Example int: EnkaGenshinGeneration().start(uids = 757562748)
----------|Example str - One UID: EnkaGenshinGeneration().start(uids = "757562748")
----------|Example str - Two or more UID: EnkaGenshinGeneration().start(uids = "757562748,544523587,874385763")
```

## Languages Supported
| Languege    |  Code   |
|-------------|---------|
|  English    |     en  |
|  русский    |     ru  |
|  Tiếng Việt |     vi  |
|  ไทย        |     th  |
|  português  |     pt  |
|  한국어      |     kr  |
|  日本語      |     jp  |
|  中文        |     zh  |
|  Indonesian |     id  |
|  français   |     fr  |
|  español    |     es  |
|  deutsch    |     de  |
|  Taiwan     |    cht  |
|  Chinese    |    chs  |

## Sample Results:

<img src="img/Example1.png" width='300' alt="Example1"/> <img src="img/Example2.png" width='300' alt="Example2"/> - The result of a custom images and adaptation.
<img src="img/Example3.png" width='300' alt="Example3"/> <img src="img/Example4.png" width='300' alt="Example4"/> - Usual result.
