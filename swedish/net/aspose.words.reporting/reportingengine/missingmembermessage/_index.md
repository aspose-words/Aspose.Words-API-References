---
title: ReportingEngine.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MissingMemberMessage i ReportingEngine, anpassa meddelanden för saknade objektmedlemmar enkelt. Förbättra användarupplevelsen utan ansträngning!
type: docs
weight: 30
url: /sv/net/aspose.words.reporting/reportingengine/missingmembermessage/
---
## ReportingEngine.MissingMemberMessage property

Hämtar eller ställer in ett strängvärde som skrivs ut istället för ett malluttryck som representerar en vanlig referens till en saknad medlem i ett objekt. Standardvärdet är en tom sträng.

```csharp
public string MissingMemberMessage { get; set; }
```

## Anmärkningar

Egenskapen bör användas tillsammans medAllowMissingMembers alternativ. Annars utlöses ett undantag när en saknad medlem i ett objekt påträffas.

Egenskapen påverkar endast utskrift av ett malluttryck som representerar en vanlig referens till en missing objektmedlem. Till exempel påverkas inte utskrift av en binär operator, vars operander refererar till en missing objektmedlem.

Värdet för den här egenskapen kan inte sättas till null.

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

* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
