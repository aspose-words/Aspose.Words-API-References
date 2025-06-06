---
title: HtmlSaveOptions.AllowNegativeIndent
linktitle: AllowNegativeIndent
articleTitle: AllowNegativeIndent
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HtmlSaveOptions AllowNegativeIndent pour contrôler les retraits de paragraphe lors de l'enregistrement au format HTML, MHTML ou EPUB. Optimisez la mise en forme de vos documents dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.saving/htmlsaveoptions/allownegativeindent/
---
## HtmlSaveOptions.AllowNegativeIndent property

Spécifie si les retraits négatifs à gauche et à droite des paragraphes sont normalisés lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`FAUX` .

```csharp
public bool AllowNegativeIndent { get; set; }
```

## Remarques

Lorsque le retrait négatif n'est pas autorisé, il est exporté sous forme de marge nulle vers HTML. Lorsque le retrait négatif est autorisé, un paragraphe peut apparaître partiellement en dehors de la fenêtre du navigateur .

## Exemples

Montre comment conserver les retraits négatifs dans le fichier .html de sortie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un tableau avec un retrait négatif, ce qui le poussera vers la gauche au-delà de la limite de page gauche.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Insérer un tableau avec un retrait positif, ce qui poussera le tableau vers la droite.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Lorsque nous enregistrons un document au format HTML, Aspose.Words ne conservera que les retraits négatifs
// comme celui que nous avons appliqué à la première table si nous définissons l'indicateur « AllowNegativeIndent »
// dans un objet SaveOptions que nous passerons à "true".
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    AllowNegativeIndent = allowNegativeIndent,
    TableWidthOutputMode = HtmlElementSizeOutputMode.RelativeOnly
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
