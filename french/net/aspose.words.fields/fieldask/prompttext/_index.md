---
title: FieldAsk.PromptText
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldAsk propriété. Obtient ou définit le texte de linvite le titre de la fenêtre dinvite.
type: docs
weight: 50
url: /fr/net/aspose.words.fields/fieldask/prompttext/
---
## FieldAsk.PromptText property

Obtient ou définit le texte de l'invite (le titre de la fenêtre d'invite).

```csharp
public string PromptText { get; set; }
```

### Exemples

Montre comment créer un champ ASK et définir ses propriétés.

```csharp
[Test]
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Placez un champ où la réponse à notre champ ASK sera placée.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // Insérez le champ ASK et modifiez ses propriétés pour référencer notre champ REF par nom de signet.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // Les champs ASK appliquent la réponse par défaut à leurs champs REF respectifs lors d'un publipostage.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Nous pouvons modifier ou remplacer la réponse par défaut dans nos champs ASK avec un répondeur personnalisé,
    // qui se produira lors d'un publipostage.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");

/// <summary>
/// Ajoute du texte à la réponse par défaut d'un champ ASK lors d'un publipostage.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### Voir également

* class [FieldAsk](../)
* espace de noms [Aspose.Words.Fields](../../fieldask/)
* Assemblée [Aspose.Words](../../../)


