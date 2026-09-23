---
title: "CurrentThreadSettings"
linktitle: "CurrentThreadSettings"
second_title: "Aspose.Words für Java"
description: "Diese Klasse hilft dabei, Locale und Zeitzone thread‑isoliert für eine Aspose.Words‑Anwendung in Java festzulegen."
type: docs
weight: 139
url: /de/java/com.aspose.words/currentthreadsettings/
---

**Inheritance:**
java.lang.Object
```
public class CurrentThreadSettings
```

Diese Klasse hilft, das thread‑isolierte Gebietsschema und die Zeitzone für eine Aspose.Words‑Anwendung festzulegen.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getLocale()](#getLocale) | Gibt java.util.Locale zurück, das vom aktuellen Aspose.Words‑Thread verwendet wird. |
| [getTimeZone()](#getTimeZone) | Gibt java.util.TimeZone zurück, das vom aktuellen Aspose.Words‑Thread verwendet wird. |
| [setLocale(String localeName)](#setLocale-java.lang.String) | Setzt java.util.Locale für den aktuellen Aspose.Words‑Thread anhand des Locale‑Namens. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale) | Setzt java.util.Locale für den aktuellen Aspose.Words‑Thread. |
| [setTimeZone(TimeZone timeZone)](#setTimeZone-java.util.TimeZone) | Setzt java.util.TimeZone für den aktuellen Aspose.Words‑Thread. |
### getLocale() {#getLocale}
```
public static Locale getLocale()
```


Gibt java.util.Locale zurück, das vom aktuellen Aspose.Words‑Thread verwendet wird.

**Returns:**
java.util.Locale
### getTimeZone() {#getTimeZone}
```
public static TimeZone getTimeZone()
```


Gibt java.util.TimeZone zurück, das vom aktuellen Aspose.Words‑Thread verwendet wird.

**Returns:**
java.util.TimeZone
### setLocale(String localeName) {#setLocale-java.lang.String}
```
public static void setLocale(String localeName)
```


Setzt java.util.Locale für den aktuellen Aspose.Words‑Thread anhand des Locale‑Namens.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| localeName | java.lang.String |  |

### setLocale(Locale locale) {#setLocale-java.util.Locale}
```
public static void setLocale(Locale locale)
```


Setzt java.util.Locale für den aktuellen Aspose.Words‑Thread.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| locale | java.util.Locale |  |

### setTimeZone(TimeZone timeZone) {#setTimeZone-java.util.TimeZone}
```
public static void setTimeZone(TimeZone timeZone)
```


Setzt java.util.TimeZone für den aktuellen Aspose.Words‑Thread.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| timeZone | java.util.TimeZone |  |

