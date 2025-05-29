---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ReportingEngine-alternativ för att enkelt anpassa beteenden vid rapportbyggande med flexibla flaggor för optimal prestanda och kontroll.
type: docs
weight: 40
url: /sv/net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

Hämtar eller ställer in en uppsättning flaggor som styr beteendet hos detta[`ReportingEngine`](../) instans när du skapar en rapport.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Exempel

Visar hur man tillåter saknade medlemmar.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Se även

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
