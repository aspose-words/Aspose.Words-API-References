---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words для .NET
description: Создавайте мощные источники данных без особых усилий с помощью конструктора XmlDataSource, загружая XML-данные с использованием оптимизированных параметров по умолчанию для бесшовной интеграции.
type: docs
weight: 10
url: /ru/net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

Создает новый источник данных с данными из XML-файла, используя параметры по умолчанию для загрузки XML-данных.

```csharp
public XmlDataSource(string xmlPath)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | String | Путь к XML-файлу, который будет использоваться в качестве источника данных. |

## Примеры

Покажите, как использовать XML в качестве источника данных (строки).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### Смотрите также

* class [XmlDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

Создает новый источник данных с данными из потока XML, используя параметры по умолчанию для загрузки данных XML.

```csharp
public XmlDataSource(Stream xmlStream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | Stream | Поток XML-данных, который будет использоваться в качестве источника данных. |

## Примеры

Покажите, как использовать XML в качестве источника данных (потока).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Смотрите также

* class [XmlDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

Создает новый источник данных с данными из XML-файла, используя файл определения схемы XML. Параметры по умолчанию используются для загрузки XML-данных.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | String | Путь к XML-файлу, который будет использоваться в качестве источника данных. |
| xmlSchemaPath | String | Путь к файлу определения схемы XML, который предоставляет схему для файла XML . |

### Смотрите также

* class [XmlDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

Создает новый источник данных с данными из потока XML, используя поток определения схемы XML. Параметры по умолчанию используются для загрузки данных XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | Stream | Поток XML-данных, который будет использоваться в качестве источника данных. |
| xmlSchemaStream | Stream | Поток определения схемы XML, который предоставляет схему для данных XML. |

### Смотрите также

* class [XmlDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

Создает новый источник данных с данными из XML-файла, используя указанные параметры загрузки XML-данных.

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | String | Путь к XML-файлу, который будет использоваться в качестве источника данных. |
| options | XmlDataLoadOptions | Варианты загрузки XML-данных. |

### Смотрите также

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

Создает новый источник данных с данными из потока XML, используя указанные параметры загрузки данных XML.

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | Stream | Поток XML-данных, который будет использоваться в качестве источника данных. |
| options | XmlDataLoadOptions | Варианты загрузки XML-данных. |

### Смотрите также

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

Создает новый источник данных с данными из XML-файла, используя файл определения схемы XML. Указанные параметры используются для загрузки XML-данных.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | String | Путь к XML-файлу, который будет использоваться в качестве источника данных. |
| xmlSchemaPath | String | Путь к файлу определения схемы XML, который предоставляет схему для файла XML . |
| options | XmlDataLoadOptions | Варианты загрузки XML-данных. |

### Смотрите также

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

Создает новый источник данных с данными из потока XML, используя поток определения схемы XML. Указанные параметры используются для загрузки данных XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | Stream | Поток XML-данных, который будет использоваться в качестве источника данных. |
| xmlSchemaStream | Stream | Поток определения схемы XML, который предоставляет схему для данных XML. |
| options | XmlDataLoadOptions | Варианты загрузки XML-данных. |

### Смотрите также

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
