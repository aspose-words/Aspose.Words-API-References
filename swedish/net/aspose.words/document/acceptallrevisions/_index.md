---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words för .NET
description: Document AcceptAllRevisions metod. Accepterar alla spårade ändringar i dokumentet i C#.
type: docs
weight: 520
url: /sv/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Accepterar alla spårade ändringar i dokumentet.

```csharp
public void AcceptAllRevisions()
```

## Anmärkningar

Denna metod är en genväg för[`AcceptAll`](../../revisioncollection/acceptall/).

## Exempel

Visar hur du accepterar alla spårningsändringar i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Redigera dokumentet medan du spårar ändringar för att skapa några ändringar.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! "); 
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// Vi kan upprepa varje revision och acceptera/förkasta den som en del av vårt dokument.
// Om vi vet att vi vill acceptera varje revidering, kan vi göra det enklare genom att anropa den här metoden.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
