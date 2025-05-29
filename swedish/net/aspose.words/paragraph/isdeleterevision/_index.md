---
title: Paragraph.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IsDeleteRevision i Microsoft Word. Lär dig hur den indikerar borttagningar under ändringsspårning för effektiv dokumenthantering.
type: docs
weight: 40
url: /sv/net/aspose.words/paragraph/isdeleterevision/
---
## Paragraph.IsDeleteRevision property

Returnerar sant om det här objektet togs bort i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsDeleteRevision { get; }
```

## Exempel

Visar hur man arbetar med revideringsparagrafer.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// Ovanstående stycken är inte revideringar.
// Stycken som vi lägger till efter att vi startat revisionsspårning kommer att registreras som "Infoga"-revisioner.
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// Stycken som vi tar bort efter att vi startat revisionsspårning kommer att registreras som "Ta bort"-revisioner.
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// Sådana stycken kommer att finnas kvar tills vi antingen accepterar eller avvisar borttagningsrevisionen.
// Att acceptera revisionen kommer att ta bort stycket permanent,
// och om du avvisar revisionen kommer den att finnas kvar i dokumentet som om vi aldrig raderade den.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Acceptera revisionen och kontrollera sedan att stycket är borta.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.AreEqual(0, para.Count);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
