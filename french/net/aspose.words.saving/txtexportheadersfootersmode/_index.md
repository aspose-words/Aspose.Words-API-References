---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words pour .NET
description: Découvrez comment l'énumération TxtExportHeadersFootersMode d'Aspose.Words améliore les exportations de texte brut en personnalisant la gestion des en-têtes et des pieds de page pour des résultats optimaux.
type: docs
weight: 6440
url: /fr/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

Spécifie la manière dont les en-têtes et les pieds de page sont exportés au format texte brut.

```csharp
public enum TxtExportHeadersFootersMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucun en-tête ni pied de page n'est exporté. |
| PrimaryOnly | `1` | Seuls les en-têtes et pieds de page principaux sont exportés au début et à la fin de chaque section. |
| AllAtEnd | `2` | Tous les en-têtes et pieds de page sont placés après tous les corps de section à la toute fin d'un document. |

## Exemples

Montre comment spécifier comment exporter les en-têtes et les pieds de page au format texte brut.

```csharp
Document doc = new Document();

// Insérer des en-têtes/pieds de page pairs et principaux dans le document.
// L'en-tête/les pieds de page principaux remplaceront les en-têtes/pieds de page pairs.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Insérer des pages pour afficher ces en-têtes et pieds de page.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Créez un objet « TxtSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Définissez la propriété « ExportHeadersFootersMode » sur « TxtExportHeadersFootersMode.None »
// pour ne pas exporter d'en-têtes/pieds de page.
// Définissez la propriété « ExportHeadersFootersMode » sur « TxtExportHeadersFootersMode.PrimaryOnly »
// pour exporter uniquement les en-têtes/pieds de page principaux.
// Définissez la propriété « ExportHeadersFootersMode » sur « TxtExportHeadersFootersMode.AllAtEnd »
// pour placer tous les en-têtes et pieds de page de tous les corps de section à la fin du document.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

string newLine = Environment.NewLine;
switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Even header{newLine}{newLine}" +
                        $"Primary header{newLine}{newLine}" +
                        $"Even footer{newLine}{newLine}" +
                        $"Primary footer{newLine}{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual($"Primary header{newLine}" +
                        $"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Primary footer{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}", docText);
        break;
}
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
