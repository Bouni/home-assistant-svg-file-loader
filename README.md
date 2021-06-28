# Home Assistant SVG File Loader

Use this to easily implement custom SVG Icons in Home Assistant. Unlike entity_picutre, this custom module will also update the icons color based on it's state.

# Install instructions

## HACS 

1. Install using [HACS](https://hacs.xyz) (Add this repo as a custom repo, then install as usual)
2. Refresh browser cache

## Manually

1. Download & Copy Files

    copy ```dist/home-assistant-svg-file-loader.js``` to your ```/config/www``` folder and create a new folder, ```svg``` for example, inside ```www```. 
    Place your custom icons in ```svg```. You can also create a deeper folder structure if you wish (/config/www/your/custom/folder/)

2. Add the Resource to Home Assistant

    Go to Configuration\Lovelace Dashboards\Resources and add a new resource. Enter ```/local/home-assistant-svg-file-loader.js``` as URL.

# Usage

Specify custom icons like this ```svg:your/custom/folder/your_icon_name``` where ```your/custom/folder/``` is the folder structure you've created for your SVG files and ```your_icon_name``` is the filename of the SVG without the file extension.

# Error Handling

If an invalid file path is specified, the module will automatically load a default icon containing a question mark.

If you want to override the default icon for certain entities, and not just the icon in a specific lovelace card, you will have to [setup customization](https://www.home-assistant.io/docs/configuration/customizing-devices/).

# Credits
Fallback icon is part of https://github.com/prasertcbs/HueIconPackPng/blob/master/LICENSE.

