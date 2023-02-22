---
title: Class FieldCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldCollection classe. Une collection deField objets qui représentent les champs dans la plage spécifiée.
type: docs
weight: 1540
url: /fr/net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

Une collection de[`Field`](../field/) objets qui représentent les champs dans la plage spécifiée.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.fields/fieldcollection/count/) { get; } | Renvoie le nombre de champs de la collection. |
| [Item](../../aspose.words.fields/fieldcollection/item/) { get; } | Renvoie un champ à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clear](../../aspose.words.fields/fieldcollection/clear/)() | Supprime tous les champs de cette collection du document et de cette collection elle-même. |
| [GetEnumerator](../../aspose.words.fields/fieldcollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [Remove](../../aspose.words.fields/fieldcollection/remove/)(Field) | Supprime le champ spécifié de cette collection et du document. |
| [RemoveAt](../../aspose.words.fields/fieldcollection/removeat/)(int) | Supprime un champ à l'index spécifié de cette collection et du document. |

### Remarques

Une instance de cette collection itère les champs qui commencent à se situer dans la plage spécifiée.

La`FieldCollection` collection ne possède pas les champs qu'elle contient, mais n'est qu'une sélection de champs.

La`FieldCollection` collection est "en direct", c'est-à-dire que les modifications apportées aux enfants du nœud object à partir duquel elle a été créée sont immédiatement reflétées dans les champs renvoyés par le`FieldCollection` propriétés et méthodes.

### Exemples

Montre comment supprimer des champs d'une collection de champs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Vous trouverez ci-dessous quatre façons de supprimer des champs d'une collection de champs.
// 1 - Récupère un champ pour se supprimer :
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Récupérer la collection pour supprimer un champ que nous passons à sa méthode de suppression :
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Supprimer un champ d'une collection à un index :
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Supprimez tous les champs de la collection d'un coup :
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Montre comment travailler avec une collection de champs.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Itérer sur la collection de champs et imprimer le contenu et le type
    // de chaque champ à l'aide d'une implémentation de visiteur personnalisée.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());

/// <summary>
/// Documenter l'implémentation du visiteur qui imprime les informations de champ.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Obtient le texte brut du document qui a été accumulé par le visiteur.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldStart est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldSeparator est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldEnd est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


