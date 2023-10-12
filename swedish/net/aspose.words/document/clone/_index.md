---
title: Document.Clone
second_title: Aspose.Words för .NET API Referens
description: Document metod. Utför en djup kopia avDocument .
type: docs
weight: 570
url: /sv/net/aspose.words/document/clone/
---
## Document.Clone method

Utför en djup kopia av[`Document`](../) .

```csharp
public Document Clone()
```

### Returvärde

Det klonade dokumentet.

### Exempel

Visar hur man djupklonar ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Kloning kommer att producera ett nytt dokument med samma innehåll som originalet,
// men med en unik kopia av var och en av originaldokumentets noder.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


