---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldChar FieldType, qui révèle le type du champ et optimise ainsi la gestion de vos données et votre efficacité en programmation. En savoir plus !
type: docs
weight: 10
url: /fr/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Renvoie le type du champ.

```csharp
public FieldType FieldType { get; }
```

## Exemples

Montre comment travailler avec un nœud FieldStart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Récupérer l'objet de façade qui représente le champ dans le document.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Mettre à jour le champ pour afficher la date actuelle.
field.Update();
```

### Voir également

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
