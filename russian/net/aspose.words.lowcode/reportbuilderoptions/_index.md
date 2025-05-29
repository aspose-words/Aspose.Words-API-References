---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words LowCode ReportBuilderOptions, разработанный для улучшения работы с LINQ Reporting Engine с помощью настраиваемых параметров для бесперебойной генерации документов.
type: docs
weight: 4380
url: /ru/net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

Представляет параметры функциональности LINQ Reporting Engine.

```csharp
public class ReportBuilderOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | Получает неупорядоченный набор (т.е. коллекцию уникальных элементов), содержащийType объекты , полностью или частично определенные имена которых могут использоваться в шаблонах отчетов, обрабатываемых этим экземпляром engine , для вызова статических членов соответствующих типов, выполнения приведения типов и т. д. |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | Возвращает или задает строковое значение, напечатанное вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Значение по умолчанию — пустая строка. |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | Возвращает или задает набор флагов, управляющих поведением этого[`ReportingEngine`](../../aspose.words.reporting/reportingengine/) экземпляр при построении отчета. |

## Примеры

Показывает, как заполнить документ данными.

```csharp
public void BuildReportData()
{
    // Существует несколько способов заполнить документ данными:
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Смотрите также

* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
