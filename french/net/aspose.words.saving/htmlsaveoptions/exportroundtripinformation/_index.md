---
title: ExportRoundtripInformation
second_title: Référence de l'API Aspose.Words pour .NET
description: Spécifie sil faut écrire les informations daller-retour lors de lenregistrement au format HTML MHTML ou EPUB. La valeur par défaut estvrai pour HTML etfaux pour MHTML et EPUB.
type: docs
weight: 250
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Spécifie s'il faut écrire les informations d'aller-retour lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`vrai` pour HTML et`faux` pour MHTML et EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

### Remarques

L'enregistrement des informations d'aller-retour permet de restaurer les propriétés du document telles que les taquets de tabulation, les commentaires , les en-têtes et les pieds de page lors du chargement des documents HTML dans un[`Document`](../../../aspose.words/document) objet.

Lorsque`vrai`, les informations aller-retour sont exportées en tant que -aw-* CSS properties des éléments HTML correspondants.

Lorsque`faux`, n'entraîne la sortie d'aucune information d'aller-retour dans les fichiers produits.

### Exemples

Montre comment conserver les éléments masqués lors de la conversion en .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Lors de la conversion d'un document en .html, certains éléments tels que les signets masqués, les positions de la forme d'origine,
// ou les notes de bas de page seront soit supprimées, soit converties en texte brut et effectivement perdues.
// L'enregistrement avec un objet HtmlSaveOptions avec ExportRoundtripInformation défini sur true préservera ces éléments.

// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions pour déterminer
// comment l'opération de sauvegarde exportera les éléments du document que HTML ne prend pas en charge ou n'utilise pas,
// tels que les signets masqués et les positions de forme d'origine.
// Si nous définissons le drapeau "ExportRoundtripInformation" sur "true", l'opération de sauvegarde conservera ces éléments.
// Si nous définissons le drapeau "ExportRoundTripInformation" sur "false", l'opération de sauvegarde supprimera ces éléments.
// Nous voudrons conserver ces éléments si nous avons l'intention de charger le HTML enregistré en utilisant Aspose.Words,
// car ils pourraient être utiles une fois de plus.
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

* class [HtmlSaveOptions](../../htmlsaveoptions)
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
