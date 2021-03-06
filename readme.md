# PyBeauty

Python module for beautifully varying RGB colour sets which can be used for setting colours anywhere!
This module basically varies RGB values in various random ranges via threading.Timer() executing continously after very
small interval of time i.e. in milliseconds hence resulting in beautiful transition of colours.

## Installation

Simply using PyPi:

```
pip install pybeauty
```

## Usage

Simply use this code (Modify according to your needs):

```python
from pybeauty import Beauty

def on_new_color(rgb_color):
    r_value = rgb_color[0]
    g_value = rgb_color[1]
    b_value = rgb_color[2]
    #Now you can do anything with the RGB values (set as background, set as text colour, etc..).

Beauty(Parameters, on_new_color) #Parameters is a dictionary for optional parameters (More about them specified below).
```

Optional Parameters that are available are listed below in Parameters section and have to be passed as a Dictionary (keys as name of parameters listed in Parameters section and value is your desired choice according to the options available for that parameter as specified in the Parameters section) which will be the first parameter for Beauty() constructor.

## Parameters
- ### mode (Optional)
  
  Specifies colour set in which the colours have to vary.
  
  - **Parameter Value Type:** str or list.
  
  - **Options for mode parameter**
    - **"dark":** Varies the colour in dark colours only (useful for dark mode projects).
    - **"light":** Varies the colour in light colours only (useful for light mode projects).
    - **[start_rgb, end_rgb]:** Varies the colour from start_rgb value (can be from 0 to 255) to end_rgb value (can be from 0 to 255).
  
  - **Default Value:** "" (i.e. varies from 0 to 255 RGB Values).

- ### start (Optional):
  
  Specefies colour in RGB format from which colours have to start varying.
  
  - **Input type for start parameter:** list [R_Value, G_Value, B_Value] (eg. [0, 0, 0] for black).
  
  - **Default Value:** [0, 0, 0] (for "dark", none or other mode parameter specified) and [255, 255, 255] (for "light" mode parameter specified).

- ### time (Optional):
  
  Specifies the time in milliseconds after which the colour is changed according to its range.
  Useful for decreasing the time when using on slow hardware for maintaining the smoothness.
  
  - **Parameter Value Type:** int.
  
  - **Default Value:** 40 ms (Just perfect for majority hardware types).
  
So go ahead and enjoy the beauty of time varying RGB colour sets!
