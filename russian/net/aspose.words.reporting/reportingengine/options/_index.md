---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ReportingEngine Options, позволяющее легко настраивать поведение построения отчетов с помощью гибких флагов для оптимальной производительности и контроля.
type: docs
weight: 40
url: /ru/net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

Возвращает или задает набор флагов, управляющих поведением этого[`ReportingEngine`](../) экземпляр при построении отчета.

```csharp
public ReportBuildOptions Options { get; set; }
```

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

### Смотрите также

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
