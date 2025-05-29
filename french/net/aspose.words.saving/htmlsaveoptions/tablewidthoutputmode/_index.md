---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: Aspose.Words pour .NET
description: Optimisez vos exportations HTML avec le mode HtmlSaveOptions TableWidthOutputMode. Contrôlez la largeur des lignes et des cellules de votre tableau pour un formatage MHTML et EPUB fluide.
type: docs
weight: 480
url: /fr/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Contrôle la manière dont les largeurs des tableaux, des lignes et des cellules sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut estAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## Remarques

Au format HTML, les éléments de tableau, de ligne et de cellule (**&lt;table&gt;** ,**&lt;tr&gt;** ,**&lt;th&gt;** ,**&lt;td&gt;**) peuvent avoir leurs largeurs spécifiées soit en unités relatives (pourcentage) soit en unités absolues. Dans un document dans Aspose.Words, les tableaux, les lignes et les cellules peuvent avoir leurs largeurs spécifiées en utilisant également des unités relatives ou absolues.

Lorsque vous convertissez un document en HTML à l'aide d'Aspose.Words, vous souhaiterez peut-être contrôler la manière dont les largeurs de tableau, de ligne et de cellule sont exportées pour affecter la manière dont le document résultant est affiché dans l'agent visuel (par exemple, un navigateur ou une visionneuse).

Utilisez cette propriété comme filtre pour spécifier les valeurs de largeur de tableau exportées vers le document de destination. Par exemple, si vous convertissez un document au format EPUB et souhaitez le consulter sur un appareil mobile, il est préférable d'éviter d'exporter des valeurs de largeur absolue. Pour ce faire, vous devez spécifier le mode de sortie.RelativeOnly ouNone afin que le spectateur sur l'appareil mobile puisse disposer le tableau pour qu'il s'adapte au mieux à la largeur de l'écran.

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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
