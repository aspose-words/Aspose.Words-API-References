---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words pour .NET
description: Effacez facilement les en-têtes et pieds de page de vos sections grâce à la méthode ClearHeadersFooters. Optimisez la mise en page de votre document pour un rendu impeccable !
type: docs
weight: 120
url: /fr/net/aspose.words/section/clearheadersfooters/
---
## ClearHeadersFooters() {#clearheadersfooters}

Efface les en-têtes et les pieds de page de cette section.

```csharp
public void ClearHeadersFooters()
```

## Remarques

Le texte de tous les en-têtes et pieds de page est effacé, mais[`HeaderFooter`](../../headerfooter/) les objets eux-mêmes ne sont pas supprimés.

Cela rend les en-têtes et les pieds de page de cette section liés aux en-têtes et aux pieds de page de la section précédente.

## Exemples

Montre comment effacer le contenu de tous les en-têtes et pieds de page d'une section.

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

// Videz tous les en-têtes et pieds de page de cette section de tout leur contenu.
// Les en-têtes et les pieds de page eux-mêmes seront toujours présents mais n'auront rien à afficher.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## ClearHeadersFooters(*bool*) {#clearheadersfooters_1}

Efface les en-têtes et les pieds de page de cette section.

```csharp
public void ClearHeadersFooters(bool preserveWatermarks)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| preserveWatermarks | Boolean | Vrai si les filigranes ne doivent pas être supprimés. |

## Remarques

Le texte de tous les en-têtes et pieds de page est effacé, mais[`HeaderFooter`](../../headerfooter/) les objets eux-mêmes ne sont pas supprimés.

Cela rend les en-têtes et les pieds de page de cette section liés aux en-têtes et aux pieds de page de la section précédente.

## Exemples

Montre comment effacer le contenu de l'en-tête et du pied de page avec ou sans filigrane.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Ajouter un filigrane en texte brut.
doc.Watermark.SetText("Aspose Watermark");

// Assurez-vous que les en-têtes et les pieds de page ont du contenu.
HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("First header", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("Second header", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("Third header", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("First footer", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("Second footer", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("Third footer", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Supprime tout le contenu de l'en-tête et du pied de page, à l'exception des filigranes.
doc.FirstSection.ClearHeadersFooters(true);

headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
Assert.AreEqual(WatermarkType.Text, doc.Watermark.Type);

// Supprime tout le contenu de l'en-tête et du pied de page, y compris les filigranes.
doc.FirstSection.ClearHeadersFooters(false);
Assert.AreEqual(WatermarkType.None, doc.Watermark.Type);
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
