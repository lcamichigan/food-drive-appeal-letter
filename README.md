# Food Drive Appeal Letter

[![Build status](https://ci.appveyor.com/api/projects/status/njbi2ne90pj81idb?svg=true)](https://ci.appveyor.com/project/lcamichigan/food-drive-appeal-letter)

This is a collection of resources for creating food drive appeal letters for
[Sigma Zeta of ΛΧΑ](http://lcamichigan.com).

## Contents

* [Getting Started](#getting-started)
* [Preparing a Letter](#preparing-a-letter)
* [Creating an InDesign File](#creating-an-indesign-file)

## Getting Started

To create a food drive appeal letter, you need:

* [Adobe InDesign](https://www.adobe.com/products/indesign.html). Visit
  https://www.adobe.com/creativecloud/plans.html for more information.

* Envelope.idml and Letter.idml. The easiest way to get Envelope.idml is to
  download it from
  https://ci.appveyor.com/project/lcamichigan/donation-appeal-letter/build/artifacts.
  The easiest way to get Letter.idml is to download it from
  https://ci.appveyor.com/project/lcamichigan/food-drive-appeal-letter/build/artifacts,
  but you can also [create your own](#creating-an-indesign-file).

* These fonts:

  | Font                                                                | Download URL                                                             |
  |---------------------------------------------------------------------|--------------------------------------------------------------------------|
  | [Damion](https://fonts.google.com/specimen/Damion)                  | https://github.com/google/fonts/raw/master/ofl/damion/Damion-Regular.ttf |
  | [Gillius](http://arkandis.tuxfamily.org/adffonts.html)              | http://arkandis.tuxfamily.org/fonts/Gillius-Collection-20110312.zip      |
  | [Linux Libertine](http://www.linuxlibertine.org) (OpenType version) | http://mirrors.ctan.org/fonts/libertine.zip                              |

## Preparing a Letter

Here is where you can find information about
[Food Gatherers](http://www.foodgatherers.org):

| To find this                          | See                                                                                   |
|---------------------------------------|---------------------------------------------------------------------------------------|
| Expenses toward hunger relief         | A newsletter at http://www.foodgatherers.org/?module=Page&sID=annualreportnewsletters |
| Feeding America membership status     | http://www.feedingamerica.org/find-your-local-foodbank/food-gatherers.html            |
| Amount to provide up to 15 meals ($5) | http://www.foodgatherers.org                                                          |

Here is where you can find information about ΛΧΑ:

| To find this                                | See                                          |
|---------------------------------------------|----------------------------------------------|
| Number of initiated members                 | https://www.lambdachi.org/aboutlca-2/        |
| Number of meals provided to Feeding America | https://www.lambdachi.org/feeding-america-2/ |

Use _number of recipients_ × 75 to estimate the number of meals if every
recipient gives $25, and use _number of recipients_ × 5 ÷ 73 to estimate the
number of people fed in a year if every recipient gives $25.

The text of the letter is intended for a fall food drive. Here is text that
could be used to introduce a Watermelon Bust:

> I’m happy to announce Sigma’s next Watermelon Bust! The Watermelon Bust is a
> competitive food drive among University of Michigan Greek organizations
> starting on Month ## and culminating in a day of watermelon-related fun and
> games at the chapter house on Month ##. We will donate the nonperishable food
> and monetary gifts we collect to Food Gatherers, a local food bank and member
> of ΛΧΑ’s philanthropy partner Feeding America. Learn more about Food Gatherers
> from its website at foodgatherers.org.

## Creating an InDesign File

Creating an InDesign IDML file from the files in this repository requires the
free [Zip](http://www.info-zip.org/Zip.html) utility. To install Zip on Windows:

1. Click ftp://ftp.info-zip.org/pub/infozip/win32/zip300xn-x64.zip to download
   zip300xn-x64.zip.

2. Right-click zip300xn-x64.zip, choose Extract All, and then click Extract to
   extract a folder named zip300xn-x64.

3. Right-click zip300xn-x64.zip in the zip300xn-x64 folder you just extracted,
   choose Extract All, and then click Extract to extract another folder named
   zip300xn-x64.

4. Move this second zip300xn-x64 folder to C:\Program Files.

Zip is included with macOS.

To create an InDesign file, first download this repository as a ZIP archive. To
do this, click
[here](https://github.com/lcamichigan/food-drive-appeal-letter/archive/master.zip).
Unzip the archive wherever you wish. Then, `cd` to the
[Letter IDML](Letter%20IDML) folder and enter in PowerShell

```powershell
& "$env:ProgramFiles\zip300xn-x64\zip" -X0 ..\Letter.idml mimetype
& "$env:ProgramFiles\zip300xn-x64\zip" --recurse-paths --no-dir-entries -X9 ..\Letter.idml * --exclude mimetype
```

or in Command Prompt

```batch
"%ProgramFiles%\zip300xn-x64\zip" -X0 ..\Letter.idml mimetype
"%ProgramFiles%\zip300xn-x64\zip" --recurse-paths --no-dir-entries -X9 ..\Letter.idml * --exclude mimetype
```

or in Terminal

```sh
zip -X0 ../Letter.idml mimetype
zip --recurse-paths --no-dir-entries -X9 ../Letter.idml * --exclude *.DS_Store mimetype
```
