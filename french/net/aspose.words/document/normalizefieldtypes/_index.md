---
title: Document.NormalizeFieldTypes
second_title: Référence de l'API Aspose.Words pour .NET
description: Document méthode. Modifie les valeurs de type de champFieldType deFieldStart FieldSeparator FieldEnd dans tout le document afin quils correspondent aux types de champs contenus dans les codes de champs.
type: docs
weight: 610
url: /fr/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Modifie les valeurs de type de champ[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) dans tout le document afin qu'ils correspondent aux types de champs contenus dans les codes de champs.

```csharp
public void NormalizeFieldTypes()
```

### Remarques

Utilisez cette méthode après les modifications du document qui affectent les types de champ.

Pour modifier les valeurs de type de champ dans une partie spécifique du document, utilisez[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

### Exemples

Montre comment mettre à jour le type d'un champ avec son code de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words détecte automatiquement les types de champs en fonction des codes de champs.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Modifiez manuellement le texte brut du champ, qui détermine le code du champ.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];

// La modification du code de champ a changé ce champ en un champ d'un type différent,
// mais les propriétés de type du champ affichent toujours l'ancien type.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Mettez à jour ces propriétés avec cette méthode pour afficher la valeur actuelle.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType); 
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


