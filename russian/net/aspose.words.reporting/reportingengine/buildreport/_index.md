---
title: BuildReport
second_title: Справочник по API Aspose.Words для .NET
description: Заполняет указанный шаблонный документ данными из указанного источника превращая его в готовый отчет.
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
| document | Document | Шаблон документа для заполнения данными. |
| dataSource | Object | Объект источника данных. |

### Возвращаемое значение

Флаг, указывающий, был ли разбор документа шаблона успешным. Возвращаемый флаг имеет смысл, только если значение свойства[`Options`](../options)включает InlineErrorMessagesопция.

### Примечания

С помощью этой перегрузки вы можете ссылаться на элементы источника данных в шаблонный документ, но вы не можете ссылаться на сам объект источника данных. Для этого следует использовать перегрузку[`BuildReport`](../buildreport) .

Объект источника данных может быть одного из следующих типов:

* [`XmlDataSource`](../../xmldatasource)
* [`JsonDataSource`](../../jsondatasource)
* [`CsvDataSource`](../../csvdatasource)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Любой другой произвольный нединамический и неанонимный тип .NET

_ x000d_

Информацию о том, как работать с источниками данных разных типов в документах-шаблонах, см. в справочнике по синтаксису шаблона (https://docs. aspose.com/display/wordsnet/Template+Syntax).

### Смотрите также

* class [Document](../../../aspose.words/document)
* class [ReportingEngine](../../reportingengine)
* namespace [Aspose.Words.Reporting](../../reportingengine)
* assembly [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Заполняет указанный шаблонный документ данными из указанного источника, превращая его в готовый отчет.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Шаблон документа для заполнения данными. |
| dataSource | Object | Объект источника данных. |
| dataSourceName | String | Имя для ссылки на объект источника данных в шаблоне. |

### Возвращаемое значение

Флаг, указывающий, был ли разбор документа шаблона успешным. Возвращаемый флаг имеет смысл, только если значение свойства[`Options`](../options)включает InlineErrorMessagesопция.

### Примечания

Используя эту перегрузку, вы можете ссылаться на элементы источника данных и сам объект источника данных в шаблоне. Если вы не собираетесь ссылаться на сам объект источника данных, вы можете опустить*dataSourceName* передачу null или использовать[`BuildReport`](../buildreport)перегрузка.

Объект источника данных может быть одного из следующих типов:

* [`XmlDataSource`](../../xmldatasource)
* [`JsonDataSource`](../../jsondatasource)
* [`CsvDataSource`](../../csvdatasource)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Любой другой произвольный нединамический и неанонимный тип .NET

_ x000d_

Информацию о том, как работать с источниками данных разных типов в документах-шаблонах, см. в справочнике по синтаксису шаблона (https://docs. aspose.com/display/wordsnet/Template+Syntax).

### Смотрите также

* class [Document](../../../aspose.words/document)
* class [ReportingEngine](../../reportingengine)
* namespace [Aspose.Words.Reporting](../../reportingengine)
* assembly [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Заполняет указанный шаблонный документ данными из указанных источников, превращая его в готовый отчет.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Шаблон документа для заполнения данными. |
| dataSources | Object[] | Массив объектов источников данных. |
| dataSourceNames | String[] | Массив имен для ссылки на объекты источников данных в шаблоне. |

### Возвращаемое значение

Флаг, указывающий, был ли разбор документа шаблона успешным. Возвращаемый флаг имеет смысл, только если значение свойства[`Options`](../options)включает InlineErrorMessagesопция.

### Примечания

С помощью этой перегрузки вы можете ссылаться на несколько объектов источников данных и их участников в шаблоне. Имя первого источника данных может быть опущено (т.е. быть пустой строкой или нулевым значением), если вы собираетесь ссылаться на члены источника данных, но не на сам объект источника данных . Имена других источников данных должны быть указаны и уникальны.

Если вы собираетесь использовать один источник данных, рассмотрите возможность использования[`BuildReport`](../buildreport) и[`BuildReport`](../buildreport)вместо этого перегружается.

Объект источника данных может быть одного из следующих типов:

* [`XmlDataSource`](../../xmldatasource)
* [`JsonDataSource`](../../jsondatasource)
* [`CsvDataSource`](../../csvdatasource)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Любой другой произвольный нединамический и неанонимный тип .NET

_ x000d_

Информацию о том, как работать с источниками данных разных типов в документах-шаблонах, см. в справочнике по синтаксису шаблона (https://docs. aspose.com/display/wordsnet/Template+Syntax).

### Смотрите также

* class [Document](../../../aspose.words/document)
* class [ReportingEngine](../../reportingengine)
* namespace [Aspose.Words.Reporting](../../reportingengine)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
