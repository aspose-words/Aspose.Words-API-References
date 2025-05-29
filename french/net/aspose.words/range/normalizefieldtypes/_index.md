---
title: Range.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words pour .NET
description: Transformez les types de champs avec la méthode NormalizeFieldTypes. Assurez-vous que FieldStart, FieldSeparator et FieldEnd correspondent aux codes de champ spécifiés pour une gestion transparente des données.
type: docs
weight: 90
url: /fr/net/aspose.words/range/normalizefieldtypes/
---
## Range.NormalizeFieldTypes method

Modifie les valeurs du type de champ[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) dans cette plage afin qu'ils correspondent aux types de champs contenus dans les codes de champ.

```csharp
public void NormalizeFieldTypes()
```

## Remarques

Utilisez cette méthode après les modifications de document qui affectent les types de champs.

Pour modifier les valeurs de type de champ dans l'ensemble du document, utilisez[`NormalizeFieldTypes`](../../document/normalizefieldtypes/).

## Exemples

Montre comment maintenir le type d'un champ à jour avec son code de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words détecte automatiquement les types de champs en fonction des codes de champ.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Modifiez manuellement le texte brut du champ, qui détermine le code du champ.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// La modification du code du champ a changé ce champ en un champ d'un type différent,
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

* class [Range](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
