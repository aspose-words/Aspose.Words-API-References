---
title: FontSubstitutionSettings
second_title: Aspose.Words for Java API Reference
description: Specifies font substitution mechanism settings.
type: docs
weight: 292
url: /java/com.aspose.words/fontsubstitutionsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionSettings
```

Specifies font substitution mechanism settings.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

Font substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

The order of the rules is following: 1. Font name substitution rule (enabled by default) 2. Font config substitution rule (disabled by default) 3. Table substitution rule (enabled by default) 4. Font info substitution rule (enabled by default) 5. Default font rule (enabled by default)

Note that font info substitution rule will always resolve the font if [FontInfo](../../com.aspose.words/fontinfo) is available and will override the default font rule. If you want to use the default font rule then you should disable the font info substitution rule.

Note that font config substitution rule will resolve the font in most cases and thus overrides all other rules.


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDefaultFontSubstitution()](#getDefaultFontSubstitution) | Settings related to default font substitution rule. |
| [getFontConfigSubstitution()](#getFontConfigSubstitution) | Settings related to font config substitution rule. |
| [getFontInfoSubstitution()](#getFontInfoSubstitution) | Settings related to font info substitution rule. |
| [getFontNameSubstitution()](#getFontNameSubstitution) | Settings related to font name substitution rule. |
| [getTableSubstitution()](#getTableSubstitution) | Settings related to table substitution rule. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDefaultFontSubstitution() {#getDefaultFontSubstitution}
```
public DefaultFontSubstitutionRule getDefaultFontSubstitution()
```


Settings related to default font substitution rule.

**Returns:**
[DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule) - The corresponding [DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule) value.
### getFontConfigSubstitution() {#getFontConfigSubstitution}
```
public FontConfigSubstitutionRule getFontConfigSubstitution()
```


Settings related to font config substitution rule.

**Returns:**
[FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule) - The corresponding [FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule) value.
### getFontInfoSubstitution() {#getFontInfoSubstitution}
```
public FontInfoSubstitutionRule getFontInfoSubstitution()
```


Settings related to font info substitution rule.

**Returns:**
[FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule) - The corresponding [FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule) value.
### getFontNameSubstitution() {#getFontNameSubstitution}
```
public FontNameSubstitutionRule getFontNameSubstitution()
```


Settings related to font name substitution rule.

**Returns:**
[FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule) - The corresponding [FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule) value.
### getTableSubstitution() {#getTableSubstitution}
```
public TableSubstitutionRule getTableSubstitution()
```


Settings related to table substitution rule.

**Returns:**
[TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule) - The corresponding [TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule) value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

