---
title: FieldMergingArgsBase.Field
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldMergingArgsBase propriété. Obtient lobjet qui représente le champ de fusion actuel.
type: docs
weight: 30
url: /fr/net/aspose.words.mailmerging/fieldmergingargsbase/field/
---
## FieldMergingArgsBase.Field property

Obtient l'objet qui représente le champ de fusion actuel.

```csharp
public FieldMergeField Field { get; }
```

### Exemples

Montre comment exécuter un publipostage avec un rappel personnalisé qui gère les données de fusion sous la forme de documents HTML.

```csharp
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
/// Si le publipostage rencontre un MERGEFIELD dont le nom commence par le préfixe "html_",
/// ce rappel analyse ses données de fusion en tant que contenu HTML et ajoute le résultat à l'emplacement du document du MERGEFIELD.
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
            // Ajoute des données HTML analysées au corps du document.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Puisque nous avons déjà inséré manuellement le contenu fusionné,
             // nous n'aurons pas besoin de répondre à cet événement en renvoyant du contenu via la propriété "Texte".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Ne fais rien.
    }
}
```

### Voir également

* class [FieldMergeField](../../../aspose.words.fields/fieldmergefield/)
* class [FieldMergingArgsBase](../)
* espace de noms [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* Assemblée [Aspose.Words](../../../)


