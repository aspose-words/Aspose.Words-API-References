---
title: HtmlSaveOptions.TableWidthOutputMode
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Contrôle la manière dont les largeurs de tableau de ligne et de cellule sont exportées vers HTML MHTML ou EPUB. La valeur par défaut estAll .
type: docs
weight: 460
url: /fr/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Contrôle la manière dont les largeurs de tableau, de ligne et de cellule sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut estAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

### Remarques

Au format HTML, les éléments tableau, ligne et cellule ( **&lt;tableau&gt;** , **&lt;tr&gt;** , **&lt;e&gt;** , **&lt;dt&gt;**) peuvent avoir leurs largeurs spécifiées en relatif (pourcentage) ou en unités absolues. Dans un document dans Aspose.Words, les tableaux, les lignes et les cellules peuvent avoir leurs largeurs spécifiées en utilisant des unités relatives ou absolues aussi.

Lorsque vous convertissez un document en HTML à l'aide de Aspose.Words, vous souhaiterez peut-être contrôler la façon dont les largeurs de table, de ligne et de cellule sont exportées pour affecter la façon dont le document résultant est affiché dans l'agent visuel (par exemple, un navigateur ou une visionneuse).

Utilisez cette propriété comme filtre pour spécifier quelles valeurs de largeur de tableau sont exportées dans le document de destination. Par exemple, si vous convertissez un document en EPUB et avez l'intention de visualiser le document sur un appareil de lecture mobile, alors vous voudrez probablement éviter exporter des valeurs de largeur absolues. Pour ce faire, vous devez spécifier le mode de sortieRelativeOnly ouNone afin que le spectateur sur l'appareil mobile puisse disposer le tableau pour qu'il s'adapte au mieux à la largeur de l'écran.

### Exemples

Montre comment conserver les retraits négatifs dans le fichier .html de sortie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un tableau avec un retrait négatif, qui le poussera vers la gauche au-delà de la limite de page gauche.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Insère un tableau avec un retrait positif, ce qui poussera le tableau vers la droite.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Lorsque nous enregistrons un document au format HTML, Aspose.Words ne conservera que les retraits négatifs
// tel que celui que nous avons appliqué à la première table si nous définissons le drapeau "AllowNegativeIndent"
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
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


