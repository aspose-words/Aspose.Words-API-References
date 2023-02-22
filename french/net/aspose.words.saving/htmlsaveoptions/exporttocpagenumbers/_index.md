---
title: HtmlSaveOptions.ExportTocPageNumbers
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Spécifie sil faut écrire les numéros de page dans la table des matières lors de lenregistrement HTML MHTML et EPUB. La valeur par défaut estfaux .
type: docs
weight: 280
url: /fr/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

Spécifie s'il faut écrire les numéros de page dans la table des matières lors de l'enregistrement HTML, MHTML et EPUB. La valeur par défaut est`faux` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

### Exemples

Montre comment afficher les numéros de page lors de l'enregistrement d'un document avec une table des matières au format .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une table des matières, puis remplit le document avec des paragraphes formatés à l'aide d'un "Titre"
// style que la table des matières prendra comme entrées. Chaque entrée affichera le paragraphe d'en-tête à gauche,
// et le numéro de page qui contient le titre à droite.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 1");
builder.Writeln("Entry 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 3");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 4");
fieldToc.UpdatePageNumbers();
doc.UpdateFields();

// Les documents HTML n'ont pas de pages. Si nous enregistrons ce document au format HTML,
// les numéros de page affichés par notre table des matières n'auront aucune signification.
// Lorsque nous enregistrons le document au format HTML, nous pouvons transmettre un objet SaveOptions pour omettre ces numéros de page de la table des matières.
// Si nous définissons le drapeau "ExportTocPageNumbers" sur "true",
// chaque entrée de table des matières affichera l'en-tête, le séparateur et le numéro de page, en préservant son apparence dans Microsoft Word.
// Si nous définissons le drapeau "ExportTocPageNumbers" sur "false",
// l'opération de sauvegarde omettra à la fois le séparateur et le numéro de page et laissera le titre de chaque entrée intact.
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 1</span>" +
        "</p>"));
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


