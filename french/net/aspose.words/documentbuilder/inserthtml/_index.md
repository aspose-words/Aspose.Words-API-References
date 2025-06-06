---
title: DocumentBuilder.InsertHtml
linktitle: InsertHtml
articleTitle: InsertHtml
second_title: Aspose.Words pour .NET
description: Améliorez sans effort vos documents avec la méthode InsertHtml de DocumentBuilder  insérez de manière transparente des chaînes HTML pour une intégration de contenu dynamique.
type: docs
weight: 380
url: /fr/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(*string*) {#inserthtml}

Insère une chaîne HTML dans le document.

```csharp
public void InsertHtml(string html)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| html | String | Une chaîne HTML à insérer dans le document. |

## Remarques

Vous pouvez utiliser cette méthode pour insérer un fragment HTML ou un document HTML entier.

## Exemples

Montre comment utiliser un générateur de documents pour insérer du contenu HTML dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// L'insertion de code HTML analyse la mise en forme de chaque élément dans une mise en forme de texte de document équivalente.
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual("Paragraph right", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

Assert.AreEqual("Implicit paragraph left", paragraphs[1].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.True(paragraphs[1].Runs[0].Font.Bold);

Assert.AreEqual("Div center", paragraphs[2].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Center, paragraphs[2].ParagraphFormat.Alignment);

Assert.AreEqual("Heading 1 left.", paragraphs[3].GetText().Trim());
Assert.AreEqual("Heading 1", paragraphs[3].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

Montre comment exécuter un publipostage avec un rappel personnalisé qui gère les données de fusion sous la forme de documents HTML.

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// Si le publipostage rencontre un MERGEFIELD dont le nom commence par le préfixe « html_ »,
/// ce rappel analyse ses données de fusion en tant que contenu HTML et ajoute le résultat à l'emplacement du document MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Appelé lorsqu'un publipostage fusionne des données dans un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Ajoutez les données HTML analysées au corps du document.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Puisque nous avons déjà inséré le contenu fusionné manuellement,
            // nous n'aurons pas besoin de répondre à cet événement en renvoyant du contenu via la propriété "Texte".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Ne rien faire.
    }
}
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertHtml(*string, bool*) {#inserthtml_2}

Insère une chaîne HTML dans le document.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| html | String | Une chaîne HTML à insérer dans le document. |
| useBuilderFormatting | Boolean | Une valeur indiquant si le formatage spécifié dans[`DocumentBuilder`](../) est utilisé comme formatage de base pour le texte importé depuis HTML. |

## Remarques

Vous pouvez utiliser cette méthode pour insérer un fragment HTML ou un document HTML entier.

Quand*useBuilderFormatting* est`FAUX` , [`DocumentBuilder`](../) Le formatage est ignoré et le texte inséré est basé sur le formatage HTML par défaut. Par conséquent, le texte s'affiche tel qu'il apparaît dans les navigateurs.

Quand*useBuilderFormatting* est`vrai` , le formatage du texte inséré est basé sur[`DocumentBuilder`](../) formatage, et le texte semble avoir été inséré avec[`Write`](../write/) .

## Exemples

Montre comment appliquer la mise en forme d'un générateur de documents lors de l'insertion de contenu HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez un alignement de texte pour le générateur, insérez un paragraphe HTML avec un alignement spécifié et un sans.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Le premier paragraphe possède un alignement spécifié. Lorsque InsertHtml analyse le code HTML,
// la valeur d'alignement de paragraphe trouvée dans le code HTML remplace toujours la valeur du générateur de documents.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// Le deuxième paragraphe n'a pas d'alignement spécifié. Sa valeur d'alignement peut être renseignée.
// par la valeur du constructeur en fonction de l'indicateur que nous avons passé à la méthode InsertHtml.
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertHtml(*string, [HtmlInsertOptions](../../htmlinsertoptions/)*) {#inserthtml_1}

Insère une chaîne HTML dans le document. Permet de spécifier des options supplémentaires.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| html | String | Une chaîne HTML à insérer dans le document. |
| options | HtmlInsertOptions | Options utilisées lorsque la chaîne HTML est insérée. |

## Remarques

Vous pouvez utiliser cette méthode pour insérer un fragment HTML ou un document HTML entier.

## Exemples

Montre comment utiliser les options lors de l'insertion de code HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// Par défaut, "DocumentBuilder.InsertHtml" insère un fragment HTML qui se termine par un élément HTML de niveau bloc,
// il ferme normalement cet élément de niveau bloc et insère un saut de paragraphe.
// En conséquence, un nouveau paragraphe vide apparaît après l'insertion du document.
// Si nous spécifions « HtmlInsertOptions.RemoveLastEmptyParagraph », ces paragraphes vides supplémentaires seront supprimés.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### Voir également

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
