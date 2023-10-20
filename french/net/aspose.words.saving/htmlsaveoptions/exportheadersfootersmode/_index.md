---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions ExportHeadersFootersMode propriété. Spécifie comment les entêtes et les pieds de page sont générés au format HTML MHTML ou EPUB. La valeur par défaut estPerSection pour HTML/MHTML etNone pour EPUB en C#.
type: docs
weight: 160
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Spécifie comment les en-têtes et les pieds de page sont générés au format HTML, MHTML ou EPUB. La valeur par défaut estPerSection pour HTML/MHTML etNone pour EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## Remarques

Il est difficile de générer des en-têtes et des pieds de page de manière significative au format HTML car le HTML n'est pas paginé.

Lorsque cette propriété estPerSection, Aspose.Words exports uniquement les en-têtes et pieds de page principaux au début et à la fin de chaque section.

Lorsqu'il estFirstSectionHeaderLastSectionFooter seuls le premier en-tête principal et le dernier pied de page principal (y compris lié au précédent) sont exportés.

Vous pouvez désactiver complètement l'exportation des en-têtes et des pieds de page en définissant cette propriété surNone.

## Exemples

Montre comment omettre les en-têtes/pieds de page lors de l’enregistrement d’un document au format HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Ce document contient des en-têtes et des pieds de page. Nous pouvons y accéder via la collection "HeadersFooters".
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Les formats tels que .html ne divisent pas le document en pages, donc les en-têtes/pieds de page ne fonctionneront pas de la même manière
// ils le feraient lorsque nous ouvririons le document au format .docx à l'aide de Microsoft Word.
// Si nous convertissons un document avec des en-têtes/pieds de page en HTML, la conversion assimilera les en-têtes/pieds de page dans le corps du texte.
// Nous pouvons utiliser un objet SaveOptions pour omettre les en-têtes/pieds de page lors de la conversion en HTML.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Ouvrez notre document enregistré et vérifiez qu'il ne contient pas le texte de l'en-tête
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Voir également

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
