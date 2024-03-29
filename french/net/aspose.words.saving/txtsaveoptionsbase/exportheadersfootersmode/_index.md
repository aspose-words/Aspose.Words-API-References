---
title: TxtSaveOptionsBase.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words pour .NET
description: TxtSaveOptionsBase ExportHeadersFootersMode propriété. Spécifie la manière dont les entêtes et les pieds de page sont exportés aux formats de texte. La valeur par défaut estPrimaryOnly  en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/
---
## TxtSaveOptionsBase.ExportHeadersFootersMode property

Spécifie la manière dont les en-têtes et les pieds de page sont exportés aux formats de texte. La valeur par défaut estPrimaryOnly .

```csharp
public TxtExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## Exemples

Montre comment spécifier comment exporter les en-têtes et les pieds de page au format texte brut.

```csharp
Document doc = new Document();

// Insère des en-têtes/pieds de page pairs et principaux dans le document.
// Les en-têtes/pieds de page principaux remplaceront les en-têtes/pieds de page pairs.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Insère des pages pour afficher ces en-têtes et pieds de page.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Crée un objet "TxtSaveOptions", que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Définit la propriété "ExportHeadersFootersMode" sur "TxtExportHeadersFootersMode.None"
// pour ne pas exporter d'en-têtes/pieds de page.
// Définit la propriété "ExportHeadersFootersMode" sur "TxtExportHeadersFootersMode.PrimaryOnly"
// pour exporter uniquement les en-têtes/pieds de page principaux.
// Définit la propriété "ExportHeadersFootersMode" sur "TxtExportHeadersFootersMode.AllAtEnd"
// pour placer tous les en-têtes et pieds de page de tous les corps de section à la fin du document.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Even header\r\n\r\n" +
                        "Primary header\r\n\r\n" +
                        "Even footer\r\n\r\n" +
                        "Primary footer\r\n\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual("Primary header\r\n" +
                        "Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Primary footer\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n", docText);
        break;
}
```

### Voir également

* enum [TxtExportHeadersFootersMode](../../txtexportheadersfootersmode/)
* class [TxtSaveOptionsBase](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
