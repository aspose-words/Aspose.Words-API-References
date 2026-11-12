---
title: "JsonSimpleValueParseMode"
linktitle: "JsonSimpleValueParseMode"
second_title: "Aspose.Words для Java"
description: "Указывает режим разбора простых значений JSON: null, boolean, number, integer и string при загрузке JSON в Java."
type: docs
weight: 410
url: /ru/java/com.aspose.words/jsonsimplevalueparsemode/
---

**Inheritance:**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

Указывает режим разбора простых значений JSON (null, boolean, number, integer и string) при загрузке JSON. Такой режим не влияет на разбор значений даты и времени.

 **Examples:** 

Показывает, как использовать JSON в качестве источника данных (строка).

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
## Поля

| Поле | Описание |
| --- | --- |
| [LOOSE](#LOOSE) | Указывает режим, при котором типы простых значений JSON определяются при разборе их строковых представлений. |
| [STRICT](#STRICT) | Указывает режим, при котором типы простых значений JSON определяются непосредственно из нотации JSON. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


Указывает режим, при котором типы простых значений JSON определяются при разборе их строковых представлений. Например, тип 'prop' из JSON‑фрагмента '\\{ prop: \"123\" \\}' определяется как integer в этом режиме.

### STRICT {#STRICT}
```
public static int STRICT
```


Указывает режим, при котором типы простых значений JSON определяются непосредственно из нотации JSON. Например, тип 'prop' из JSON‑фрагмента '\\{ prop: \"123\" \\}' определяется как string в этом режиме.

### length {#length}
```
public static int length
```


### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**Returns:**
int
### getName(int jsonSimpleValueParseMode) {#getName-int}
```
public static String getName(int jsonSimpleValueParseMode)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
