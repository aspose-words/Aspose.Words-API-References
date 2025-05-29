---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldDocVariable VariableName pour gérer facilement les variables de vos documents. Simplifiez la recherche et optimisez la gestion de vos documents dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

Obtient ou définit le nom de la variable de document à récupérer.

```csharp
public string VariableName { get; set; }
```

## Exemples

Montre comment utiliser les champs DOCPROPERTY pour afficher les propriétés et les variables du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux manières d'utiliser les champs DOCPROPERTY.
// 1 - Afficher une propriété intégrée :
// Définissez une valeur personnalisée pour la propriété intégrée « Catégorie », puis insérez un champ DOCPROPERTY qui y fait référence.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 - Afficher une variable de document personnalisée :
// Définissez une variable personnalisée, puis référencez cette variable avec un champ DOCPROPERTY.
Assert.AreEqual(0, doc.Variables.Count);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### Voir également

* class [FieldDocVariable](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
