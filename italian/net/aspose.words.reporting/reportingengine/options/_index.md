---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words per .NET
description: Scopri la proprietà Opzioni di ReportingEngine per personalizzare facilmente i comportamenti di creazione dei report con flag flessibili per prestazioni e controllo ottimali.
type: docs
weight: 40
url: /it/net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

Ottiene o imposta un set di flag che controllano il comportamento di questo[`ReportingEngine`](../) istanza durante la creazione di un report.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Esempi

Mostra come consentire l'accesso ai membri mancanti.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Guarda anche

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
