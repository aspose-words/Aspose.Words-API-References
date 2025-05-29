---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ReportingEngine-Optionen“, um das Verhalten beim Erstellen von Berichten mit flexiblen Flags für optimale Leistung und Kontrolle einfach anzupassen.
type: docs
weight: 40
url: /de/net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

Ruft eine Reihe von Flags ab oder setzt diese, die das Verhalten dieses[`ReportingEngine`](../) Instanz beim Erstellen eines Berichts.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Beispiele

Zeigt, wie fehlende Mitglieder zugelassen werden.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Siehe auch

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
