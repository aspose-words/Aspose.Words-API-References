---
title: "MeasurementUnits"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words для Java"
description: "Указывает единицу измерения в Java."
type: docs
weight: 460
url: /ru/java/com.aspose.words/measurementunits/
---

**Inheritance:**
java.lang.Object
```
public class MeasurementUnits
```

Указывает единицу измерения.

 **Examples:** 

Показывает, как сделать сохранённый документ соответствующим более старой схеме ODT.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(OdtSaveMeasureUnit.CENTIMETERS);
     saveOptions.isStrictSchema11(exportToOdt11Specs);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Сантиметры. |
| [INCHES](#INCHES) | Дюймы. |
| [MILLIMETERS](#MILLIMETERS) | Миллиметры. |
| [PICAS](#PICAS) | Пика (обычно используется в традиционном межсимвольном интервале печатных машин). |
| [POINTS](#POINTS) | Пункты. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String measurementUnitsName)](#fromName-java.lang.String) |  |
| [getName(int measurementUnits)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int measurementUnits)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Сантиметры.

### INCHES {#INCHES}
```
public static int INCHES
```


Дюймы.

### MILLIMETERS {#MILLIMETERS}
```
public static int MILLIMETERS
```


Миллиметры.

### PICAS {#PICAS}
```
public static int PICAS
```


Пика (обычно используется в традиционном межсимвольном интервале печатных машин).

### POINTS {#POINTS}
```
public static int POINTS
```


Пункты.

### length {#length}
```
public static int length
```


### fromName(String measurementUnitsName) {#fromName-java.lang.String}
```
public static int fromName(String measurementUnitsName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| measurementUnitsName | java.lang.String |  |

**Returns:**
int
### getName(int measurementUnits) {#getName-int}
```
public static String getName(int measurementUnits)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| measurementUnits | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int measurementUnits) {#toString-int}
```
public static String toString(int measurementUnits)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| measurementUnits | int |  |

**Returns:**
java.lang.String
