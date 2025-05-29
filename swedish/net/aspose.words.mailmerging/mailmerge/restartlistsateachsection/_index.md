---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words för .NET
description: Upptäck egenskapen RestartListsAtEachSection för MailMerge – kontrolllistor återställs i varje avsnitt för sömlösa dokumentkopplingar. Förbättra din dokumentprecision idag!
type: docs
weight: 110
url: /sv/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Hämtar eller anger ett värde som anger om listor startas om i varje avsnitt efter att en dokumentkoppling har utförts.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Anmärkningar

Standardvärdet är`sann` .

## Exempel

Visar hur man styr om listnumreringen startas om i varje avsnitt när dokumentkoppling utförs.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
