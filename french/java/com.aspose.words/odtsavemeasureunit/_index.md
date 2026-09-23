---
title: "OdtSaveMeasureUnit"
linktitle: "OdtSaveMeasureUnit"
second_title: "Aspose.Words pour Java"
description: "Unités de mesure spécifiées à appliquer au contenu mesurable du document, comme les largeurs de formes et autres, lors de l'enregistrement en Java."
type: docs
weight: 494
url: /fr/java/com.aspose.words/odtsavemeasureunit/
---

**Inheritance:**
java.lang.Object
```
public class OdtSaveMeasureUnit
```

Unités de mesure spécifiées à appliquer au contenu mesurable du document tel que les formes, les largeurs et autres lors de l'enregistrement.

 **Examples:** 

Montre comment utiliser différentes unités de mesure pour définir les paramètres de style d'un document ODT enregistré.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // When we export the document to .odt, we can use an OdtSaveOptions object to modify how we save the document.
 // We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Centimeters"
 // to define content such as style parameters using the metric system, which Open Office uses.
 // We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Inches"
 // to define content such as style parameters using the imperial system, which Microsoft Word uses.
 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(odtSaveMeasureUnit);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Spécifie que le contenu du document est enregistré en centimètres. |
| [INCHES](#INCHES) | Spécifie que le contenu du document est enregistré en pouces. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String odtSaveMeasureUnitName)](#fromName-java.lang.String) |  |
| [getName(int odtSaveMeasureUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odtSaveMeasureUnit)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Spécifie que le contenu du document est enregistré en centimètres.

### INCHES {#INCHES}
```
public static int INCHES
```


Spécifie que le contenu du document est enregistré en pouces.

### length {#length}
```
public static int length
```


### fromName(String odtSaveMeasureUnitName) {#fromName-java.lang.String}
```
public static int fromName(String odtSaveMeasureUnitName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| odtSaveMeasureUnitName | java.lang.String |  |

**Returns:**
int
### getName(int odtSaveMeasureUnit) {#getName-int}
```
public static String getName(int odtSaveMeasureUnit)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| odtSaveMeasureUnit | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int odtSaveMeasureUnit) {#toString-int}
```
public static String toString(int odtSaveMeasureUnit)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| odtSaveMeasureUnit | int |  |

**Returns:**
java.lang.String
