---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words för .NET
description: Kopiera enkelt dina dokument med vår dokumentkloningsmetod. Få precisa djupa kopior för sömlös redigering och effektivt arbetsflöde.
type: docs
weight: 590
url: /sv/net/aspose.words/document/clone/
---
## Document.Clone method

Utför en djup kopiering av[`Document`](../) .

```csharp
public Document Clone()
```

### Returvärde

Det klonade dokumentet.

## Exempel

Visar hur man djupklonar ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Kloning skapar ett nytt dokument med samma innehåll som originalet,
// men med en unik kopia av var och en av originaldokumentets noder.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
