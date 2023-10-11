---
title: Document.NormalizeFieldTypes
second_title: Référence de l'API Aspose.Words pour .NET
description: Document méthode. Modifie les valeurs du type de champFieldType deFieldStart FieldSeparator FieldEnd dans tout le document afin quils correspondent aux types de champs contenus dans les codes de champs.
type: docs
weight: 650
url: /fr/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Modifie les valeurs du type de champ[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) dans tout le document afin qu'ils correspondent aux types de champs contenus dans les codes de champs.

```csharp
public void NormalizeFieldTypes()
```

### Remarques

Utilisez cette méthode après les modifications du document affectant les types de champs.

Pour modifier les valeurs du type de champ dans une partie spécifique du document, utilisez[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

### Exemples

Montre comment mettre à jour le type d'un champ avec son code de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words détecte automatiquement les types de champs en fonction des codes de champ.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Modifie manuellement le texte brut du champ, qui détermine le code du champ.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// La modification du code du champ a modifié ce champ en un champ d'un type différent,
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


