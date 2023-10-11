---
title: IFieldUserPromptRespondent.Respond
second_title: Référence de l'API Aspose.Words pour .NET
description: IFieldUserPromptRespondent méthode. Une fois implémenté renvoie une réponse de lutilisateur à linvite. Votre implémentation devrait renvoyernul pour indiquer que lutilisateur na pas répondu à linvite cestàdire que lutilisateur a appuyé sur le bouton Annuler dans la fenêtre dinvite.
type: docs
weight: 10
url: /fr/net/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent.Respond method

Une fois implémenté, renvoie une réponse de l'utilisateur à l'invite. Votre implémentation devrait renvoyer`nul` pour indiquer que l'utilisateur n'a pas répondu à l'invite (c'est-à-dire que l'utilisateur a appuyé sur le bouton Annuler dans la fenêtre d'invite).

```csharp
public string Respond(string promptText, string defaultResponse)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| promptText | String | Texte d'invite (c'est-à-dire titre de la fenêtre d'invite). |
| defaultResponse | String | Réponse utilisateur par défaut (c'est-à-dire valeur initiale contenue dans la fenêtre d'invite). |

### Return_Value

Réponse de l'utilisateur (c'est-à-dire valeur confirmée contenue dans la fenêtre d'invite).

### Exemples

Montre comment créer un champ ASK et définir ses propriétés.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Placez un champ où sera placée la réponse à notre champ ASK.
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
}

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

* interface [IFieldUserPromptRespondent](../)
* espace de noms [Aspose.Words.Fields](../../ifielduserpromptrespondent/)
* Assemblée [Aspose.Words](../../../)


