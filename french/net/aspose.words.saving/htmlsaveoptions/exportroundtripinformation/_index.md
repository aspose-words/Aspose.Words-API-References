---
title: HtmlSaveOptions.ExportRoundtripInformation
linktitle: ExportRoundtripInformation
articleTitle: ExportRoundtripInformation
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ExportRoundtripInformation de HtmlSaveOptions pour contrôler les données aller-retour aux formats HTML, MHTML et EPUB. Optimisez vos exportations dès aujourd'hui !
type: docs
weight: 240
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Spécifie s'il faut écrire les informations aller-retour lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`vrai` pour HTML et`FAUX` pour MHTML et EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

## Remarques

La sauvegarde des informations aller-retour permet de restaurer les propriétés du document telles que les taquets de tabulation, les commentaires, les en-têtes et les pieds de page lors du chargement des documents HTML dans un[`Document`](../../../aspose.words/document/) objet.

Quand`vrai`, les informations aller-retour sont exportées sous la forme -aw-* CSS properties des éléments HTML correspondants.

Quand`FAUX`, ne provoque aucune sortie d'informations aller-retour dans les fichiers produits.

## Exemples

Montre comment conserver les éléments cachés lors de la conversion en .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Lors de la conversion d'un document en .html, certains éléments tels que les signets cachés, les positions de forme d'origine,
// ou les notes de bas de page seront soit supprimées, soit converties en texte brut et seront effectivement perdues.
// L'enregistrement avec un objet HtmlSaveOptions avec ExportRoundtripInformation défini sur true conservera ces éléments.

// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions pour déterminer
// comment l'opération de sauvegarde exportera les éléments du document que HTML ne prend pas en charge ou n'utilise pas,
// tels que les signets cachés et les positions de forme d'origine.
// Si nous définissons l'indicateur « ExportRoundtripInformation » sur « true », l'opération de sauvegarde conservera ces éléments.
// Si nous définissons l'indicateur « ExportRoundTripInformation » sur « false », l'opération de sauvegarde supprimera ces éléments.
// Nous voudrons conserver ces éléments si nous avons l'intention de charger le code HTML enregistré à l'aide d'Aspose.Words,
// car ils pourraient être utiles à nouveau.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.True(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    Assert.True(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"));

    Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
else
{
    Assert.True(outDocContents.Contains("<div style=\"clear:both\">"));
    Assert.True(outDocContents.Contains("<span>&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number 1</span>"));

    Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
