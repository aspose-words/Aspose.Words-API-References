---
title: Paragraph.IsInsertRevision
second_title: Aspose.Words för .NET API Referens
description: Paragraph fast egendom. Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad.
type: docs
weight: 110
url: /sv/net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsInsertRevision { get; }
```

### Exempel

Visar hur man arbetar med revisionsstycken.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// Ovanstående stycken är inte ändringar.
// Stycken som vi lägger till efter att vi har startat revisionsspårning kommer att registreras som "Infoga" revisioner.
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// Stycken som vi tar bort efter att vi har startat revisionsspårning kommer att registreras som "Radera" revisioner.
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// Sådana stycken kommer att finnas kvar tills vi antingen accepterar eller avvisar raderingsrevisionen.
// Om du accepterar omarbetningen tas stycket bort för gott,
// och att avvisa revisionen kommer att lämna den i dokumentet som om vi aldrig tagit bort den.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Acceptera revisionen och verifiera sedan att stycket är borta.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.That(para, Is.Empty);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)


