---
title: FieldChar.IsLocked
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldChar propriété. Obtient ou définit si le champ parent est verrouillé ne doit pas recalculer son résultat.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

Obtient ou définit si le champ parent est verrouillé (ne doit pas recalculer son résultat).

```csharp
public bool IsLocked { get; set; }
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

// Met à jour le champ pour afficher la date actuelle.
field.Update();
```

### Voir également

* class [FieldChar](../)
* espace de noms [Aspose.Words.Fields](../../fieldchar/)
* Assemblée [Aspose.Words](../../../)


