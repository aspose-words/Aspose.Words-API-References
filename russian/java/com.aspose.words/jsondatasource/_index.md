---
title: "JsonDataSource"
linktitle: "JsonDataSource"
second_title: "Aspose.Words для Java"
description: "Обеспечивает доступ к данным JSON‑файла или потока для использования в отчёте на Java."
type: docs
weight: 409
url: /ru/java/com.aspose.words/jsondatasource/
---

**Inheritance:**
java.lang.Object
```
public class JsonDataSource
```

Предоставляет доступ к данным JSON-файла или потока, которые будут использоваться в отчете.

Чтобы узнать больше, посетите статью документации [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Чтобы получить доступ к данным соответствующего файла или потока при генерации отчёта, передайте экземпляр этого класса в качестве источника данных в один из методов [ReportingEngine](../../com.aspose.words/reportingengine/). перегрузки buildReport.

В шаблонных документах, если верхнеуровневый элемент JSON является массивом, экземпляр [JsonDataSource](../../com.aspose.words/jsondatasource/) следует рассматривать так же, как если бы это был экземпляр [DataTable](../../com.aspose.words.net.system.data/datatable/). Если верхнеуровневый элемент JSON является объектом, экземпляр [JsonDataSource](../../com.aspose.words/jsondatasource/) следует рассматривать так же, как если бы это был экземпляр [DataRow](../../com.aspose.words.net.system.data/datarow/). Для получения дополнительной информации см. справку по синтаксису шаблонов (https://docs.aspose.com/display/wordsjava/Template+Syntax).

В шаблонных документах вы можете работать с типизированными значениями элементов JSON. Для удобства движок заменяет набор простых типов JSON следующим:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Движок автоматически распознаёт значения дополнительных типов по их JSON‑представлениям.

Чтобы переопределить поведение загрузки данных JSON по умолчанию, инициализируйте и передайте экземпляр [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) в конструктор этого класса.

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


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String) | Создаёт новый источник данных с данными из JSON‑файла, используя параметры по умолчанию для разбора JSON‑данных. |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream) | Инициализирует новый экземпляр этого класса. |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions) | Создаёт новый источник данных с данными из JSON‑файла, используя указанные параметры для разбора JSON‑данных. |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions) | Инициализирует новый экземпляр этого класса. |
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String}
```
public JsonDataSource(String jsonPath)
```


Создаёт новый источник данных с данными из JSON‑файла, используя параметры по умолчанию для разбора JSON‑данных.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonPath | java.lang.String | Путь к JSON‑файлу, который будет использоваться в качестве источника данных. |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream}
```
public JsonDataSource(InputStream jsonStream)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


Создаёт новый источник данных с данными из JSON‑файла, используя указанные параметры для разбора JSON‑данных.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonPath | java.lang.String | Путь к JSON‑файлу, который будет использоваться в качестве источника данных. |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) | Параметры разбора JSON‑данных. |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) |  |

