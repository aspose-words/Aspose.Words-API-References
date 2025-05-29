---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: Découvrez le type de champ Microsoft Word grâce à notre propriété « Type de champ ». Améliorez vos documents grâce à une mise en forme précise et des fonctionnalités de contenu dynamique.
type: docs
weight: 100
url: /fr/net/aspose.words.fields/field/type/
---
## Field.Type property

Obtient le type de champ Microsoft Word.

```csharp
public virtual FieldType Type { get; }
```

## Exemples

Montre comment insérer un champ dans un document à l'aide d'un code de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Cette surcharge de la méthode InsertField met automatiquement à jour les champs insérés.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Voir également

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
