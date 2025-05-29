---
title: FieldOptions.FieldUpdatingCallback
linktitle: FieldUpdatingCallback
articleTitle: FieldUpdatingCallback
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldOptions FieldUpdatingCallback pour gérer facilement les implémentations IFieldUpdatingCallback et améliorer l'efficacité de votre gestion des données.
type: docs
weight: 120
url: /fr/net/aspose.words.fields/fieldoptions/fieldupdatingcallback/
---
## FieldOptions.FieldUpdatingCallback property

Obtient ou définit[`IFieldUpdatingCallback`](../../ifieldupdatingcallback/) implémentation

```csharp
public IFieldUpdatingCallback FieldUpdatingCallback { get; set; }
```

## Exemples

Montre comment utiliser les méthodes de rappel lors d'une mise à jour de champ.

```csharp
public void FieldUpdatingCallbackTest()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");

    FieldUpdatingCallback callback = new FieldUpdatingCallback();
    doc.FieldOptions.FieldUpdatingCallback = callback;

    doc.UpdateFields();

    Assert.True(callback.FieldUpdatedCalls.Contains("Updating John Doe"));
}

/// <summary>
/// Implémentez cette interface si vous souhaitez que vos propres méthodes personnalisées soient appelées lors d'une mise à jour de champ.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// Une méthode définie par l'utilisateur qui est appelée juste avant la mise à jour d'un champ.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdating(Field field)
    {
        if (field.Type == FieldType.FieldAuthor)
        {
            FieldAuthor fieldAuthor = (FieldAuthor) field;
            fieldAuthor.AuthorName = "Updating John Doe";
        }
    }

    /// <summary>
    /// Une méthode définie par l'utilisateur qui est appelée juste après la mise à jour d'un champ.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdated(Field field)
    {
        FieldUpdatedCalls.Add(field.Result);
    }

    void IFieldUpdatingProgressCallback.Notify(FieldUpdatingProgressArgs args)
    {
        Console.WriteLine($"{args.UpdateCompleted}/{args.TotalFieldsCount}");
        Console.WriteLine($"{args.UpdatedFieldsCount}");
    }

    public IList<string> FieldUpdatedCalls { get; }
}
```

### Voir également

* interface [IFieldUpdatingCallback](../../ifieldupdatingcallback/)
* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
