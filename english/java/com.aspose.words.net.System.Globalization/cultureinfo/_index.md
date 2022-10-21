---
title: CultureInfo
second_title: Aspose.Words for Java API Reference
description: Map for .Nets System.Globalization.CultureInfo.
type: docs
weight: 10
url: /java/com.aspose.words.net.system.globalization/cultureinfo/
---

**Inheritance:**
java.lang.Object
```
public class CultureInfo
```

Map for .Net's System.Globalization.CultureInfo.
## Constructors

| Constructor | Description |
| --- | --- |
| [CultureInfo(String cultureName)](#CultureInfo-java.lang.String-) | Constructor with .Net-style Culture Name. |
| [CultureInfo(String cultureName, boolean useUserOverride)](#CultureInfo-java.lang.String-boolean-) | Constructor with .Net-style Culture Name. |
| [CultureInfo(Locale locale)](#CultureInfo-java.util.Locale-) | Constructor with Java-style Locale. |
## Methods

| Method | Description |
| --- | --- |
| [getLocale(System.Globalization.CultureInfo cultureInfo)](#getLocale-com.aspose.words.net.System.Globalization.CultureInfo-) | Gets java Locale from .Net-style CultureInfo |
| [getDateTimeFormat()](#getDateTimeFormat--) | Gets .Net-style DateTimeFormatInfo |
### CultureInfo(String cultureName) {#CultureInfo-java.lang.String-}
```
public CultureInfo(String cultureName)
```


Constructor with .Net-style Culture Name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cultureName | java.lang.String |  |

### CultureInfo(String cultureName, boolean useUserOverride) {#CultureInfo-java.lang.String-boolean-}
```
public CultureInfo(String cultureName, boolean useUserOverride)
```


Constructor with .Net-style Culture Name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cultureName | java.lang.String |  |
| useUserOverride | boolean |  |

### CultureInfo(Locale locale) {#CultureInfo-java.util.Locale-}
```
public CultureInfo(Locale locale)
```


Constructor with Java-style Locale.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| locale | java.util.Locale |  |

### getLocale(System.Globalization.CultureInfo cultureInfo) {#getLocale-com.aspose.words.net.System.Globalization.CultureInfo-}
```
public Locale getLocale(System.Globalization.CultureInfo cultureInfo)
```


Gets java Locale from .Net-style CultureInfo

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cultureInfo | [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) |  |

**Returns:**
java.util.Locale
### getDateTimeFormat() {#getDateTimeFormat--}
```
public System.Globalization.DateTimeFormatInfo getDateTimeFormat()
```


Gets .Net-style DateTimeFormatInfo

**Returns:**
[DateTimeFormatInfo](../../com.aspose.words.net.system.globalization/datetimeformatinfo)
