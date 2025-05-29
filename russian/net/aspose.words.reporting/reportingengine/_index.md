---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words для .NET
description: Откройте для себя мощную автоматизацию документов с помощью Aspose.Words.ReportingEngine. Легко заполняйте шаблоны данными и настраивайте параметры для бесперебойной отчетности.
type: docs
weight: 5470
url: /ru/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Предоставляет процедуры для заполнения шаблонов документов данными и набор настроек для управления этими процедурами.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) документальная статья.

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
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Получает неупорядоченный набор (т.е. коллекцию уникальных элементов), содержащийType объекты , полностью или частично определенные имена которых могут использоваться в шаблонах отчетов, обрабатываемых этим экземпляром engine , для вызова статических членов соответствующих типов, выполнения приведения типов и т. д. |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | Возвращает или задает строковое значение, напечатанное вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Значение по умолчанию — пустая строка. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Возвращает или задает набор флагов, управляющих поведением этого`ReportingEngine` экземпляр при построении отчета. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Возвращает или задает значение, указывающее, оптимизированы ли вызовы пользовательских типов членов, выполняемые через API отражения, с использованием динамической генерации классов или нет. Значение по умолчанию:`истинный` . |

## Методы

| Имя | Описание |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Заполняет указанный шаблон документа данными из указанного источника, превращая его в готовый отчет. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Заполняет указанный шаблон документа данными из указанного источника, превращая его в готовый отчет. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Заполняет указанный шаблон документа данными из указанных источников, превращая его в готовый отчет. |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | Возвращает типы, какие члены, а также какие члены производных типов должны быть недоступны движку через синтаксис шаблона. |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | Указывает типы, какие члены, а также какие члены производных типов должны быть недоступны движку через синтаксис шаблона. |

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)
