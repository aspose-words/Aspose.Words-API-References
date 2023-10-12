---
title: Field.Remove
second_title: Référence de l'API Aspose.Words pour .NET
description: Field méthode. Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier child de son nœud parent renvoie son paragraphe parent. Si le champ est déjà supprimé renvoienul .
type: docs
weight: 120
url: /fr/net/aspose.words.fields/field/remove/
---
## Field.Remove method

Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` .

```csharp
public Node Remove()
```

### Exemples

Montre comment supprimer des champs d’une collection de champs.

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
// 1 - Récupère un champ à supprimer :
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Récupère la collection pour supprimer un champ que l'on passe à sa méthode de suppression :
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Supprime un champ d'une collection à un index :
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Supprimez tous les champs de la collection d'un coup :
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Montre comment traiter les champs PRIVÉS.

```csharp
public void FieldPrivate()
{
    // Ouvrez un document Corel WordPerfect que nous avons converti au format .docx.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // Les documents WordPerfect 5.x/6.x comme celui que nous avons chargé peuvent contenir des champs PRIVÉS.
    // Microsoft Word préserve les champs PRIVÉS lors des opérations de chargement/sauvegarde,
    // mais ne leur fournit aucune fonctionnalité.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Nous pouvons également insérer des champs PRIVATE à l'aide d'un générateur de documents.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Ces champs ne constituent pas un moyen viable de protéger les informations sensibles.
    // Sauf si la rétrocompatibilité avec les anciennes versions de WordPerfect est essentielle,
    // nous pouvons supprimer ces champs en toute sécurité. Nous pouvons le faire en utilisant une implémentation de DocumentVisiitor.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Supprime tous les champs PRIVÉS rencontrés.
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldEnd est rencontré dans le document.
    /// Si le nœud appartient à un champ PRIVATE, l'intégralité du champ est supprimée.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### Voir également

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../field/)
* Assemblée [Aspose.Words](../../../)


