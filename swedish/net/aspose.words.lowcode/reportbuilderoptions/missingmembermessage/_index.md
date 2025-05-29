---
title: ReportBuilderOptions.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MissingMemberMessage i ReportBuilderOptions. Anpassa enkelt meddelanden för saknade objektreferenser och förbättra användarupplevelsen utan ansträngning.
type: docs
weight: 30
url: /sv/net/aspose.words.lowcode/reportbuilderoptions/missingmembermessage/
---
## ReportBuilderOptions.MissingMemberMessage property

Hämtar eller ställer in ett strängvärde som skrivs ut istället för ett malluttryck som representerar en vanlig referens till en saknad medlem i ett objekt. Standardvärdet är en tom sträng.

```csharp
public string MissingMemberMessage { get; set; }
```

## Anmärkningar

Egenskapen bör användas tillsammans medAllowMissingMembers alternativ. Annars utlöses ett undantag när en saknad medlem i ett objekt påträffas.

Egenskapen påverkar endast utskrift av ett malluttryck som representerar en vanlig referens till en missing objektmedlem. Till exempel påverkas inte utskrift av en binär operator, vars operander refererar till en missing objektmedlem.

Värdet för den här egenskapen kan inte sättas till null.

### Se även

* class [ReportBuilderOptions](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
