---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HtmlSaveOptions ExportRelativeFontSize pour personnaliser la taille des polices aux formats HTML, MHTML ou EPUB. Améliorez la lisibilité en toute simplicité !
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

Dans de nombreux documents existants (HTML, IDPF, EPUB), les tailles de police sont spécifiées en unités relatives. Cela permet aux applications d'ajuster la taille du texte lors de la visualisation et du traitement des documents. Par exemple, Microsoft Internet Explorer propose un sous-menu « Affichage - Taille du texte », tandis qu'Adobe Digital Editions propose deux boutons : Augmenter/Diminuer la taille du texte. Si vous souhaitez que cette fonctionnalité soit opérationnelle, définissez-la.`ExportRelativeFontSize` propriété à`vrai` .

Le modèle de document Aspose Words utilise et fonctionne uniquement avec des unités de taille de police absolues. Les unités relatives nécessitent une logique supplémentaire pour être recalculées à partir d'une taille initiale (standard). Taille de police de**Normale** Le style de document est considéré comme standard. Par exemple,**Normale** a une police de 12 pt et une partie du texte est de 18 pt, alors ce sera output comme**1,5 em.** au HTML.

Lorsque cette option est activée, les éléments du document autres que le texte conservent des tailles absolues. Certains attributs textuels peuvent également être exprimés de manière absolue. En particulier, l'interligne spécifié avec la règle « exactement » peut produire des résultats indésirables lors de la mise à l'échelle du texte. Par conséquent, les documents sources doivent être correctement conçus et testés lors de l'exportation avec cette règle.`ExportRelativeFontSize` réglé sur`vrai`.

## Exemples

Montre comment utiliser des tailles de police relatives lors de l'enregistrement au format .html.

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
// Définissez l'indicateur « ExportRelativeFontSize » sur « true » pour déclarer les tailles de police
 // en utilisant l'unité de mesure « em », qui est un facteur qui multiplie la taille de police actuelle.
// Définissez l'indicateur « ExportRelativeFontSize » sur « false » pour déclarer les tailles de police
// en utilisant l'unité de mesure « pt », qui est la taille absolue de la police en points.
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
