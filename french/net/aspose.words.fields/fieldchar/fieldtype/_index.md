---
title: FieldChar.FieldType
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldChar propriété. Renvoie le type du champ.
type: docs
weight: 10
url: /fr/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Renvoie le type du champ.

```csharp
public FieldType FieldType { get; }
```

### Exemples

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

// Récupère l'objet façade qui représente le champ dans le document.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Mettez à jour le champ pour afficher la date actuelle.
field.Update();
```

### Voir également

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* espace de noms [Aspose.Words.Fields](../../fieldchar/)
* Assemblée [Aspose.Words](../../../)


