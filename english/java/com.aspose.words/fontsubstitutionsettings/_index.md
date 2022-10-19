---
title: FontSubstitutionSettings
second_title: Aspose.Words for Java API Reference
description: Specifies font substitution mechanism settings.
type: docs
weight: 290
url: /java/com.aspose.words/fontsubstitutionsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionSettings
```

Specifies font substitution mechanism settings.

To learn more, visit the **Working with Fonts** documentation article.

Font substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

The order of the rules is following: 1. Font name substitution rule (enabled by default) 2. Font config substitution rule (disabled by default) 3. Table substitution rule (enabled by default) 4. Font info substitution rule (enabled by default) 5. Default font rule (enabled by default)

Note that font info substitution rule will always resolve the font if [FontInfo](../../com.aspose.words/fontinfo) is available and will override the default font rule. If you want to use the default font rule then you should disable the font info substitution rule.

Note that font config substitution rule will resolve the font in most cases and thus overrides all other rules.
## Methods

| Method | Description |
| --- | --- |
| [getTableSubstitution()](#getTableSubstitution--) | Settings related to table substitution rule. |
| [getFontInfoSubstitution()](#getFontInfoSubstitution--) | Settings related to font info substitution rule. |
| [getDefaultFontSubstitution()](#getDefaultFontSubstitution--) | Settings related to default font substitution rule. |
| [getFontConfigSubstitution()](#getFontConfigSubstitution--) | Settings related to font config substitution rule. |
| [getFontNameSubstitution()](#getFontNameSubstitution--) | Settings related to font name substitution rule. |
### getTableSubstitution() {#getTableSubstitution--}
```
public TableSubstitutionRule getTableSubstitution()
```


Settings related to table substitution rule.

**Returns:**
[TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule) - The corresponding [TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule) value.
### getFontInfoSubstitution() {#getFontInfoSubstitution--}
```
public FontInfoSubstitutionRule getFontInfoSubstitution()
```


Settings related to font info substitution rule.

**Returns:**
[FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule) - The corresponding [FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule) value.
### getDefaultFontSubstitution() {#getDefaultFontSubstitution--}
```
public DefaultFontSubstitutionRule getDefaultFontSubstitution()
```


Settings related to default font substitution rule.

**Returns:**
[DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule) - The corresponding [DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule) value.
### getFontConfigSubstitution() {#getFontConfigSubstitution--}
```
public FontConfigSubstitutionRule getFontConfigSubstitution()
```


Settings related to font config substitution rule.

**Returns:**
[FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule) - The corresponding [FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule) value.
### getFontNameSubstitution() {#getFontNameSubstitution--}
```
public FontNameSubstitutionRule getFontNameSubstitution()
```


Settings related to font name substitution rule.

**Returns:**
[FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule) - The corresponding [FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule) value.
