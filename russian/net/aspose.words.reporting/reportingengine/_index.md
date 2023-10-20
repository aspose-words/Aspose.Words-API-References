---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words для .NET
description: Aspose.Words.Reporting.ReportingEngine сорт. Предоставляет процедуры для заполнения документовшаблонов данными и набор настроек для управления этими процедурами на С#.
type: docs
weight: 4730
url: /ru/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Предоставляет процедуры для заполнения документов-шаблонов данными и набор настроек для управления этими процедурами.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) статья документации.

```csharp
public class ReportingEngine
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ReportingEngine](reportingengine/)() | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Получает неупорядоченный набор (т. е. коллекцию уникальных элементов), содержащийTypeобъекты , полные или частичные имена которых могут использоваться в шаблонах отчетов, обрабатываемых этим экземпляром engine , для вызова статических членов соответствующих типов, выполнения приведения типов и т. д. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Получает или устанавливает набор флагов, управляющих поведением этого`ReportingEngine` экземпляр при построении отчета. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Получает или задает значение, указывающее, оптимизированы ли вызовы членов пользовательского типа, выполняемые через API отражения, с использованием динамического создания классов или нет. Значение по умолчанию:`истинный` . |

## Методы

| Имя | Описание |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Заполняет указанный шаблонный документ данными из указанного источника, превращая его в готовый отчет. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Заполняет указанный шаблонный документ данными из указанного источника, превращая его в готовый отчет. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Заполняет указанный шаблонный документ данными из указанных источников, превращая его в готовый отчет. |
| [Equals](../../aspose.words.reporting/reportingengine/equals/)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [GetHashCode](../../aspose.words.reporting/reportingengine/gethashcode/)() | Служит хеш-функцией для этого типа. |

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)
