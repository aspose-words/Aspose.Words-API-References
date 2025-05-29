---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words pour .NET
description: Gérez facilement les propriétés des résultats de champ. Accédez au texte entre les séparateurs de champs ou modifiez-le pour une gestion simplifiée des données et une efficacité accrue.
type: docs
weight: 70
url: /fr/net/aspose.words.fields/field/result/
---
## Field.Result property

Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ.

```csharp
public string Result { get; set; }
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

* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
