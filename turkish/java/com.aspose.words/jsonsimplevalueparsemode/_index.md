---
title: "JsonSimpleValueParseMode"
linktitle: "JsonSimpleValueParseMode"
second_title: "Aspose.Words Java için"
description: "JSON'u Java'da yüklerken JSON basit değerleri null, boolean, sayı, tamsayı ve dize ayrıştırmak için bir mod belirtir."
type: docs
weight: 410
url: /tr/java/com.aspose.words/jsonsimplevalueparsemode/
---

**Inheritance:**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

JSON yüklenirken JSON basit değerleri (null, boolean, sayı, tamsayı ve dize) ayrıştırmak için bir mod belirtir. Böyle bir mod tarih‑zaman değerlerinin ayrıştırılmasını etkilemez.

 **Examples:** 

JSON'u bir veri kaynağı (dize) olarak nasıl kullanacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [LOOSE](#LOOSE) | JSON basit değerlerinin türlerinin, dize temsillerinin ayrıştırılması sırasında belirlendiği modu belirtir. |
| [STRICT](#STRICT) | JSON basit değerlerinin türlerinin, doğrudan JSON gösteriminden belirlendiği modu belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


JSON basit değerlerinin, dize temsillerinin ayrıştırılması sırasında belirlendiği modu belirtir. Örneğin, "\{ prop: \"123\" \}" JSON parçacığındaki 'prop' öğesinin türü bu modda tamsayı olarak belirlenir.

### STRICT {#STRICT}
```
public static int STRICT
```


JSON basit değerlerinin, doğrudan JSON gösteriminden belirlendiği modu belirtir. Örneğin, "\{ prop: \"123\" \}" JSON parçacığındaki 'prop' öğesinin türü bu modda dize olarak belirlenir.

### length {#length}
```
public static int length
```


### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**Returns:**
int
### getName(int jsonSimpleValueParseMode) {#getName-int}
```
public static String getName(int jsonSimpleValueParseMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int jsonSimpleValueParseMode) {#toString-int}
```
public static String toString(int jsonSimpleValueParseMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
