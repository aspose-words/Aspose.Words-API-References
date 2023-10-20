---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words för .NET
description: MailMerge RestartListsAtEachSection fast egendom. Hämtar eller ställer in ett värde som anger om listor startas om vid varje sektion efter körning av en epostsammanfogning i C#.
type: docs
weight: 110
url: /sv/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Hämtar eller ställer in ett värde som anger om listor startas om vid varje sektion efter körning av en e-postsammanfogning.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Anmärkningar

Standardvärdet är`Sann` .

## Exempel

Visar hur man kontrollerar om listnumrering ska startas om eller inte vid varje avsnitt när kopplingen utförs.

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
