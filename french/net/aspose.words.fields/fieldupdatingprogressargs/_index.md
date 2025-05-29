---
title: FieldUpdatingProgressArgs Class
linktitle: FieldUpdatingProgressArgs
articleTitle: FieldUpdatingProgressArgs
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldUpdatingProgressArgs, qui améliore l'automatisation de vos documents en fournissant des mises à jour en temps réel sur la progression des champs.
type: docs
weight: 2980
url: /fr/net/aspose.words.fields/fieldupdatingprogressargs/
---
## FieldUpdatingProgressArgs class

Fournit des données pour l'événement de progression de la mise à jour du champ.

```csharp
public sealed class FieldUpdatingProgressArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [TotalFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/totalfieldscount/) { get; } | Obtient le nombre total de champs à mettre à jour. |
| [UpdateCompleted](../../aspose.words.fields/fieldupdatingprogressargs/updatecompleted/) { get; } | Obtient une valeur indiquant si la mise à jour du champ est terminée. |
| [UpdatedFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/updatedfieldscount/) { get; } | Obtient le nombre de champs mis à jour. |

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

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
