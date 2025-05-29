---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words för .NET
description: Effektivisera din redigeringsprocess med metoden AcceptAllRevisions, och acceptera enkelt alla spårade ändringar i ditt dokument för en polerad slutversion.
type: docs
weight: 540
url: /sv/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Accepterar alla spårade ändringar i dokumentet.

```csharp
public void AcceptAllRevisions()
```

## Anmärkningar

Den här metoden är en genväg för[`AcceptAll`](../../revisioncollection/acceptall/).

## Exempel

Visar hur man accepterar alla spårningsändringar i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Redigera dokumentet medan du spårar ändringar för att skapa några revideringar.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! ");
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// Vi kan iterera igenom varje revision och acceptera/avvisa den som en del av vårt dokument.
// Om vi vet att vi vill acceptera varje revision kan vi göra det enklare genom att anropa den här metoden.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
