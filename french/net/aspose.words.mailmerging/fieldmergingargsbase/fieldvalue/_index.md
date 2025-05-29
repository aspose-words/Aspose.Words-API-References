---
title: FieldMergingArgsBase.FieldValue
linktitle: FieldValue
articleTitle: FieldValue
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldValue de FieldMergingArgsBase. Accédez et modifiez facilement les valeurs des champs de votre source de données pour une gestion optimisée des données.
type: docs
weight: 50
url: /fr/net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

Obtient ou définit la valeur du champ à partir de la source de données.

```csharp
public object FieldValue { get; set; }
```

## Remarques

Cette propriété contient une valeur qui vient d'être sélectionnée dans votre source de données pour ce champ par le moteur de publipostage. Vous pouvez également remplacer cette valeur en définissant la propriété.

## Exemples

Montre comment modifier les valeurs que les MERGEFIELD reçoivent lors d'un publipostage.

```csharp
public void FieldFormats()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insérez quelques MERGEFIELD avec des commutateurs de format qui modifieront les valeurs qu'ils recevront lors d'un publipostage.
    builder.InsertField("MERGEFIELD text_Field1 \\* Caps", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD text_Field2 \\* Upper", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD numeric_Field1 \\# 0.0", null);

    builder.Document.MailMerge.FieldMergingCallback = new FieldValueMergingCallback();

    builder.Document.MailMerge.Execute(
        new string[] { "text_Field1", "text_Field2", "numeric_Field1" },
        new object[] { "Field 1", "Field 2", 10 });
    string t = doc.GetText().Trim();
    Assert.AreEqual("Merge Value For \"Text_Field1\": Field 1, MERGE VALUE FOR \"TEXT_FIELD2\": FIELD 2, 10000.0", doc.GetText().Trim());
}

/// <summary>
/// Modifie les valeurs que les MERGEFIELD reçoivent lors d'un publipostage.
/// Le nom d'un MERGEFIELD doit avoir un préfixe pour que ce rappel prenne effet sur sa valeur.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// Appelé lorsqu'un publipostage fusionne des données dans un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs e)
    {
        if (e.FieldName.StartsWith("text_"))
            e.FieldValue = $"Merge value for \"{e.FieldName}\": {(string)e.FieldValue}";
        else if (e.FieldName.StartsWith("numeric_"))
            e.FieldValue = (int)e.FieldValue * 1000;
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        // Ne rien faire.
    }
}
```

### Voir également

* class [FieldMergingArgsBase](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
