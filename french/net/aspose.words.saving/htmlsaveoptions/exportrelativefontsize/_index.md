---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions ExportRelativeFontSize propriété. Spécifie si les tailles de police doivent être affichées en unités relatives lors de lenregistrement au format HTML MHTML ou EPUB. La valeur par défaut estFAUX  en C#.
type: docs
weight: 230
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

Spécifie si les tailles de police doivent être affichées en unités relatives lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`FAUX` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## Remarques

Dans de nombreux documents existants (HTML, IDPF EPUB), les tailles de police sont spécifiées en unités relatives. Cela permet aux applications d'ajuster la taille du texte lors de la visualisation/du traitement des documents. Par exemple, Microsoft Internet Explorer a un sous-menu « Affichage-&gt;Taille du texte », Adobe Digital Editions a deux boutons : Augmenter/Diminuer la taille du texte. Si vous vous attendez à ce que cette fonctionnalité fonctionne, définissez`ExportRelativeFontSize` propriété à`vrai` .

Le modèle de document Aspose Words contient et fonctionne uniquement avec des unités de taille de police absolue. Les unités relatives nécessitent une logique supplémentaire pour être recalculées à partir d'une taille initiale (standard). Taille de police de**Normale** le style de document est pris en standard. Par exemple, si**Normale** a une police de 12 pts et du texte de 18 pts, il sera alors affiché sous la forme**1,5em.** au HTML.

Lorsque cette option est activée, les éléments du document autres que le texte auront toujours des tailles absolues. Certains attributs liés au texte peuvent également être exprimés de manière absolue. En particulier, l'espacement des lignes spécifié avec la règle « exactement » peut produire des résultats indésirables lors de la mise à l'échelle du texte. Les documents sources doivent donc être correctement conçus et testés lors de l'exportation avec`ExportRelativeFontSize` mis à`vrai`.

## Exemples

Montre comment utiliser les tailles de police relatives lors de l'enregistrement au format .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions
// pour déterminer s'il faut utiliser des tailles de police relatives ou absolues.
// Définit le flag "ExportRelativeFontSize" sur "true" pour déclarer les tailles de police
 // en utilisant l'unité de mesure "em", qui est un facteur qui multiplie la taille de police actuelle.
// Définit le flag "ExportRelativeFontSize" sur "false" pour déclarer les tailles de police
// en utilisant l'unité de mesure "pt", qui est la taille absolue de la police en points.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRelativeFontSize = exportRelativeFontSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
