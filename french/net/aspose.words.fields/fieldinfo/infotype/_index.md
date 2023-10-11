---
title: FieldInfo.InfoType
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldInfo propriété. Obtient ou définit le type de propriété de document à insérer.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldinfo/infotype/
---
## FieldInfo.InfoType property

Obtient ou définit le type de propriété de document à insérer.

```csharp
public string InfoType { get; set; }
```

### Exemples

Montre comment travailler avec les champs INFO.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez une valeur pour la propriété intégrée "Commentaires", puis insérez un champ INFO pour afficher la valeur de cette propriété.
doc.BuiltInDocumentProperties.Comments = "My comment";
FieldInfo field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.Update();

Assert.AreEqual(" INFO  Comments", field.GetFieldCode());
Assert.AreEqual("My comment", field.Result);

builder.Writeln();

// Définition d'une valeur pour la propriété NewValue du champ et mise à jour
// le champ écrasera également la propriété intégrée correspondante par la nouvelle valeur.
field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.NewValue = "New comment";
field.Update();

Assert.AreEqual(" INFO  Comments \"New comment\"", field.GetFieldCode());
Assert.AreEqual("New comment", field.Result);
Assert.AreEqual("New comment", doc.BuiltInDocumentProperties.Comments);

doc.Save(ArtifactsDir + "Field.INFO.docx");
```

### Voir également

* class [FieldInfo](../)
* espace de noms [Aspose.Words.Fields](../../fieldinfo/)
* Assemblée [Aspose.Words](../../../)


