---
title: "ColorPrintMode"
linktitle: "ColorPrintMode"
second_title: "Aspose.Words per Java"
description: "Specifica come vengono stampate le pagine non colorate se il dispositivo supporta la stampa a colori in Java."
type: docs
weight: 106
url: /it/java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

Specifica come vengono stampate le pagine non colorate se il dispositivo supporta la stampa a colori.
## Campi

| Campo | Descrizione |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | Le pagine non colorate, se rilevate, vengono stampate in scala di grigi. |
| [NORMAL](#NORMAL) | Tutte le pagine vengono stampate in base alle capacità e alle impostazioni della stampante. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String colorPrintModeName)](#fromName-java.lang.String) |  |
| [getName(int colorPrintMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorPrintMode)](#toString-int) |  |
### GRAYSCALE_AUTO {#GRAYSCALE-AUTO}
```
public static int GRAYSCALE_AUTO
```


Le pagine non colorate, se rilevate, vengono stampate in scala di grigi.

 **Remarks:** 

PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) viene impostato automaticamente su false per le pagine non colorate rilevate. Se la stampante non supporta la stampa a colori, questa impostazione viene ignorata.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Tutte le pagine vengono stampate in base alle capacità e alle impostazioni della stampante.

### length {#length}
```
public static int length
```


### fromName(String colorPrintModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorPrintModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int colorPrintMode) {#toString-int}
```
public static String toString(int colorPrintMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
