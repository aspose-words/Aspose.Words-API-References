---
title: "JsonSimpleValueParseMode"
linktitle: "JsonSimpleValueParseMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد وضعًا لتحليل قيم JSON البسيطة null و boolean و number و integer و string أثناء تحميل JSON في Java."
type: docs
weight: 410
url: /ar/java/com.aspose.words/jsonsimplevalueparsemode/
---

**Inheritance:**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

يحدد وضعًا لتحليل قيم JSON البسيطة (null، boolean، number، integer، و string) أثناء تحميل JSON. هذا الوضع لا يؤثر على تحليل قيم التاريخ والوقت.

 **Examples:** 

يوضح كيفية استخدام JSON كمصدر بيانات (سلسلة).

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [LOOSE](#LOOSE) | يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة عند تحليل تمثيلاتهم النصية. |
| [STRICT](#STRICT) | يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة من تدوين JSON نفسه. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة عند تحليل تمثيلاتهم النصية. على سبيل المثال، يتم تحديد نوع 'prop' من مقطع JSON '\{ prop: "123" \}' كعدد صحيح في هذا الوضع.

### STRICT {#STRICT}
```
public static int STRICT
```


يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة من تدوين JSON نفسه. على سبيل المثال، يتم تحديد نوع 'prop' من مقطع JSON '\{ prop: "123" \}' كسلسلة نصية في هذا الوضع.

### length {#length}
```
public static int length
```


### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**Returns:**
int
### getName(int jsonSimpleValueParseMode) {#getName-int}
```
public static String getName(int jsonSimpleValueParseMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
