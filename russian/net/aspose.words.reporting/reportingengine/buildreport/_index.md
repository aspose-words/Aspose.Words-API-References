---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words для .NET
description: Создавайте готовые к использованию отчеты без усилий с помощью метода BuildReport ReportingEngine, легко заполняя шаблоны данными из выбранного вами источника.
type: docs
weight: 50
url: /ru/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Заполняет указанный шаблон документа данными из указанного источника, превращая его в готовый отчет.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Шаблон документа для заполнения данными. |
| dataSource | Object | Объект источника данных. |

### Возвращаемое значение

Флаг, указывающий, был ли анализ шаблона документа успешным. Возвращаемый флаг имеет смысл только в том случае, если значение[`Options`](../options/) свойство включает в себя InlineErrorMessages вариант.

## Примечания

Используя эту перегрузку, вы можете ссылаться на элементы источника данных в шаблонном документе, но вы не можете ссылаться на сам объект источника данных. Вам следует использовать`BuildReport` перегрузка для достижения этого.

Объект источника данных может быть одного из следующих типов:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Любой другой произвольный нединамический и неанонимный тип .NET

Информацию о том, как работать с источниками данных разных типов в шаблонах документов, см. в справочнике по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Смотрите также

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Заполняет указанный шаблон документа данными из указанного источника, превращая его в готовый отчет.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Шаблон документа для заполнения данными. |
| dataSource | Object | Объект источника данных. |
| dataSourceName | String | Имя для ссылки на объект источника данных в шаблоне. |

### Возвращаемое значение

Флаг, указывающий, был ли анализ шаблона документа успешным. Возвращаемый флаг имеет смысл только в том случае, если значение[`Options`](../options/) свойство включает в себя InlineErrorMessages вариант.

## Примечания

Используя эту перегрузку, вы можете ссылаться на элементы источника данных и сам объект источника данных в шаблоне. Если вы не собираетесь ссылаться на сам объект источника данных, вы можете опустить*dataSourceName* прохождение`нулевой` или используйте`BuildReport` перегрузка.

Объект источника данных может быть одного из следующих типов:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Любой другой произвольный нединамический и неанонимный тип .NET

Информацию о том, как работать с источниками данных разных типов в шаблонах документов, см. в справочнике по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Примеры

Показывает, как разрешить отсутствующих участников.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

Показывает, как выборочно удалять абзацы.

```csharp
// Шаблон содержит теги с восклицательным знаком. Для таких тегов пустые абзацы будут удалены.
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

Показывает, как отображать значения в виде текста в долларах.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("<<[ds.Value1]:dollarText>>\r<<[ds.Value2]:dollarText>>");

NumericTestClass testData = new NumericTestBuilder().WithValues(1234, 5621718.589).Build();

ReportingEngine report = new ReportingEngine();
report.KnownTypes.Add(typeof(NumericTestClass));
report.BuildReport(doc, testData, "ds");

doc.Save(ArtifactsDir + "ReportingEngine.DollarTextFormat.docx");
```

### Смотрите также

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Заполняет указанный шаблон документа данными из указанных источников, превращая его в готовый отчет.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Шаблон документа для заполнения данными. |
| dataSources | Object[] | Массив объектов источника данных. |
| dataSourceNames | String[] | Массив имен для ссылки на объекты источника данных в шаблоне. |

### Возвращаемое значение

Флаг, указывающий, был ли анализ шаблона документа успешным. Возвращаемый флаг имеет смысл только в том случае, если значение[`Options`](../options/) свойство включает в себя InlineErrorMessages вариант.

## Примечания

Используя эту перегрузку, вы можете ссылаться на несколько объектов источников данных и их членов в шаблоне. Имя первого источника данных может быть опущено (т. е. может быть пустой строкой или`нулевой` если вы собираетесь ссылаться на элементы источника данных , а не на сам объект источника данных. Имена других источников данных должны быть указаны и уникальны.

Если вы собираетесь использовать один источник данных, рассмотрите возможность использования`BuildReport` и`BuildReport` вместо этого перегружает.

Объект источника данных может быть одного из следующих типов:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Любой другой произвольный нединамический и неанонимный тип .NET

Информацию о том, как работать с источниками данных разных типов в шаблонах документов, см. в справочнике по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Примеры

Показывает, как работать с диаграммами в Word 2016.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

Показывает, как сохранить вставленную нумерацию как есть.

```csharp
// По умолчанию нумерованные списки из шаблонного документа продолжаются, если их идентификаторы совпадают с идентификаторами из вставляемого документа.
// При использовании "-sourceNumbering" нумерация должна быть разделена и сохранена как есть.
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### Смотрите также

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
