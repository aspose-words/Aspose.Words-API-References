---
title: ReportingEngine.BuildReport
second_title: Справочник по API Aspose.Words для .NET
description: ReportingEngine метод. Заполняет указанный шаблонный документ данными из указанного источника превращая его в готовый отчет.
type: docs
weight: 40
url: /ru/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

Заполняет указанный шаблонный документ данными из указанного источника, превращая его в готовый отчет.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Документ-шаблон для заполнения данными. |
| dataSource | Object | Объект источника данных. |

### Возвращаемое значение

Флаг, указывающий, был ли анализ документа-шаблона успешным. Возвращенный флаг имеет смысл только в том случае, если значение[`Options`](../options/)свойство включает InlineErrorMessages вариант.

### Примечания

Используя эту перегрузку, вы можете ссылаться на элементы источника данных в документе-шаблоне, но не можете ссылаться на сам объект источника данных. Вам следует использовать`BuildReport` перегрузка для достижения этой цели.

Объект источника данных может относиться к одному из следующих типов:

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

Информацию о том, как работать с источниками данных разных типов в документах шаблонов, см. в справочнике по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Смотрите также

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../reportingengine/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Заполняет указанный шаблонный документ данными из указанного источника, превращая его в готовый отчет.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Документ-шаблон для заполнения данными. |
| dataSource | Object | Объект источника данных. |
| dataSourceName | String | Имя для ссылки на объект источника данных в шаблоне. |

### Возвращаемое значение

Флаг, указывающий, был ли анализ документа-шаблона успешным. Возвращенный флаг имеет смысл только в том случае, если значение[`Options`](../options/)свойство включает InlineErrorMessages вариант.

### Примечания

Используя эту перегрузку, вы можете ссылаться на элементы источника данных и сам объект источника данных в шаблоне. Если вы не собираетесь ссылаться на сам объект источника данных, вы можете опустить*dataSourceName* прохождение`нулевой` или используйте`BuildReport` перегрузка.

Объект источника данных может относиться к одному из следующих типов:

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

Информацию о том, как работать с источниками данных разных типов в документах шаблонов, см. в справочнике по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Смотрите также

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../reportingengine/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Заполняет указанный шаблонный документ данными из указанных источников, превращая его в готовый отчет.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Документ-шаблон для заполнения данными. |
| dataSources | Object[] | Массив объектов источника данных. |
| dataSourceNames | String[] | Массив имен для ссылки на объекты источника данных в шаблоне. |

### Возвращаемое значение

Флаг, указывающий, был ли анализ документа-шаблона успешным. Возвращенный флаг имеет смысл только в том случае, если значение[`Options`](../options/)свойство включает InlineErrorMessages вариант.

### Примечания

Используя эту перегрузку, вы можете ссылаться на несколько объектов источника данных и их членов в шаблоне. Имя первого источника данных может быть опущено (т.е. должно быть пустой строкой или`нулевой`), если вы собираетесь ссылаться на элементы источника данных, но не на сам объект источника данных. Имена других источников данных должны быть указаны и уникальны.

Если вы собираетесь использовать один источник данных, рассмотрите возможность использования`BuildReport` и`BuildReport` вместо этого перегружаются.

Объект источника данных может относиться к одному из следующих типов:

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

Информацию о том, как работать с источниками данных разных типов в документах шаблонов, см. в справочнике по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Смотрите также

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../reportingengine/)
* сборка [Aspose.Words](../../../)


