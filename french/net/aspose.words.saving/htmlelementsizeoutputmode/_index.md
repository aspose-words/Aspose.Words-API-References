---
title: Enum HtmlElementSizeOutputMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.HtmlElementSizeOutputMode énumération. Spécifie comment Aspose.Words exporte les largeurs et hauteurs des éléments au format HTML MHTML et EPUB.
type: docs
weight: 5060
url: /fr/net/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enumeration

Spécifie comment Aspose.Words exporte les largeurs et hauteurs des éléments au format HTML, MHTML et EPUB.

```csharp
public enum HtmlElementSizeOutputMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| All | `0` | Toutes les tailles d'éléments, en unités absolues et relatives, spécifiées dans le document sont exportées. |
| RelativeOnly | `1` | Les tailles des éléments sont exportées uniquement si elles sont spécifiées en unités relatives dans le document. Les tailles fixes ne sont pas exportées dans ce mode. Les agents visuels calculeront les tailles manquantes pour rendre la mise en page du document plus naturelle. |
| None | `2` | Les tailles des éléments ne sont pas exportées. Les agents visuels construiront automatiquement la mise en page en fonction de la relation entre les éléments. |

### Exemples

Montre comment conserver les retraits négatifs dans le fichier .html de sortie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un tableau avec un retrait négatif, ce qui le poussera vers la gauche au-delà de la limite gauche de la page.
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
// comme celui que nous avons appliqué à la première table si nous définissons le flag "AllowNegativeIndent"
// dans un objet SaveOptions que l'on passera à "true".
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

* property [TableWidthOutputMode](../htmlsaveoptions/tablewidthoutputmode/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


