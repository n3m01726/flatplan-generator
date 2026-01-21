# **Flatplan Generator – Adobe InDesign**
Automatic flatplan generator for Adobe InDesign based on CSV data. This script allows you to quickly create pagination mockups with a modular structure and maintainable code.

## 🚀 **Features**

* **Automatic generation**: Creates complete flatplans from a CSV file
* **Color management**: Automatic assignment of pastel colors by section
* **Advertising support**: Specialized handling of ads with fractional formats (1/2, 1/3, 1/4)
* **Smart pagination**: Automatic calculation of positions and spreads
* **Visual separators**: Separator lines every 4 pages to ease printing
* **Modular structure**: Code organized into reusable modules

## 📁 **Project structure**

```
flatplan-generator/
├── constants.jsx          # Configuration and constants
├── utilities.jsx          # Utility functions
├── colorManager.jsx       # Color management
├── layoutCalculator.jsx   # Positioning calculations  
├── cardBuilder.jsx        # Visual element construction
├── start.jsx              # Main orchestration file
└── README.md
```

## 📋 **Prerequisites**

* Adobe InDesign (recent versions tested)
* InDesign template: `gabarit_pagin.indt` with the required masters
* Required masters: **“A-Master”** and **“B-Master”**
* A CSV file formatted according to the expected structure

## 📊 **CSV file format**
The CSV file must contain the following columns:

```
startPage,title,section,pageCount,advertiser,sector
1,"Main article",Editorial,2,,
3,"Toyota advertisement",Advertising,1,Toyota,Automotive
4,"News",News,3,,
```

## 🛠️ **Installation and usage**

**Method 1: Modular files (recommended)**

* Place all `.jsx` files in the same folder
* Adjust the template path in `constants.jsx`:

```js
var PATHS = {
    templateFile: "path/to/your/template.indt"
};
```

* Run `start.jsx` in Adobe InDesign

**Method 2: Manual loading**
Load the files in the following order in InDesign:

1. `constants.jsx`
2. `utilities.jsx`
3. `colorManager.jsx`
4. `layoutCalculator.jsx`
5. `cardBuilder.jsx`
6. `start.jsx`

## ⚙️ **Configuration**
Edit `constants.jsx` to customize:

* Card dimensions: width, section heights
* Colors: pastel color palette
* File paths: template and logs
* Text styles: sizes and alignments

## 🎨 **Advanced features**

**Advertising management**

* Support for fractional formats (1/2, 1/3, 1/4 page)
* Grey overlay with ad number
* Special formatting: “Advertiser – Sector”

**Color system**

* Automatic assignment by section
* 16 predefined pastel colors
* Consistent color reuse

**Smart pagination**

* Automatic spread calculation
* Multi-page handling
* Automatic master application

## 🐛 **Debugging**

* Errors are automatically logged to `indesign_script_errors.log`
* Alert messages in case of issues
* Modular structure for easier debugging

## 🤝 **Contribution**
This modular structure facilitates collaboration:

* Each module has a specific responsibility
* Easily extensible code
* Clear separation of concerns

## 📝 **License**
Project developed for automated flatplan generation in an editorial production environment.
