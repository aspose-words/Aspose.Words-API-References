---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words pour .NET
description: Section ClearHeadersFooters méthode. Efface les entêtes et pieds de page de cette section en C#.
type: docs
weight: 100
url: /fr/net/aspose.words/section/clearheadersfooters/
---
## Section.ClearHeadersFooters method

Efface les en-têtes et pieds de page de cette section.

```csharp
public void ClearHeadersFooters()
```

## Remarques

Le texte de tous les en-têtes et pieds de page est effacé, mais[`HeaderFooter`](../../headerfooter/) les objets eux-mêmes ne sont pas supprimés.

Cela rend les en-têtes et pieds de page de cette section liés aux en-têtes et pieds de page de la section précédente.

## Exemples

Montre comment effacer le contenu de tous les en-têtes et pieds de page d’une section.

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Vide tous les en-têtes et pieds de page de cette section de tout leur contenu.
// Les en-têtes et pieds de page eux-mêmes seront toujours présents mais n'auront rien à afficher.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
