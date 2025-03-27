---
title: TableSubstitutionRule class
linktitle: TableSubstitutionRule class
articleTitle: TableSubstitutionRule class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fonts.TableSubstitutionRule class. Table font substitution rule"
type: docs
weight: 250
url: /nodejs-net/Aspose.Words.Fonts/tablesubstitutionrule/
---

## TableSubstitutionRule class

Table font substitution rule.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/nodejs-net/working-with-fonts/) documentation article.




### Remarks

This rule defines the list of substitute font names to be used if the original font is not available.
Substitutes will be checked for the font name and the [FontInfo.altName](../fontinfo/altName/) (if any).



**Inheritance:** [TableSubstitutionRule](./) → [FontSubstitutionRule](../fontsubstitutionrule/)

### Properties

| Name | Description |
| --- | --- |
| [enabled](../fontsubstitutionrule/enabled/) | Specifies whether the rule is enabled or not.<br>(Inherited from [FontSubstitutionRule](../fontsubstitutionrule/)) |

### Methods

| Name | Description |
| --- | --- |
|[ addSubstitutes(originalFontName, substituteFontNames)](./addSubstitutes/#string_string[]) | Adds substitute font names for given original font name. |
|[ getSubstitutes(originalFontName)](./getSubstitutes/#string) | Returns array containing substitute font names for the specified original font name. |
|[ load(fileName)](./load/#string) | Loads table substitution settings from XML file. |
|[ load(stream)](./load/#buffer) | Loads table substitution settings from XML stream. |
|[ loadAndroidSettings()](./loadAndroidSettings/#default) | Loads predefined table substitution settings for Android platform. |
|[ loadLinuxSettings()](./loadLinuxSettings/#default) | Loads predefined table substitution settings for Linux platform. |
|[ loadWindowsSettings()](./loadWindowsSettings/#default) | Loads predefined table substitution settings for Windows platform. |
|[ save(fileName)](./save/#string) | Saves the current table substitution settings to file. |
|[ save(outputStream)](./save/#buffer) | Saves the current table substitution settings to stream. |
|[ setSubstitutes(originalFontName, substituteFontNames)](./setSubstitutes/#string_string[]) | Override substitute font names for given original font name. |

### See Also

* module [Aspose.Words.Fonts](../)
* class [FontSubstitutionRule](../fontsubstitutionrule/)

