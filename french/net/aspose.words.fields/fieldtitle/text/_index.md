---
title: FieldTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Gérez facilement votre propriété Texte du Titre du Champ. Obtenez ou définissez facilement le texte du titre pour une meilleure clarté et une meilleure expérience utilisateur dans votre application.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Obtient ou définit le texte du titre.

```csharp
public string Text { get; set; }
```

## Exemples

Montre comment utiliser le champ TITRE.

```csharp
Document doc = new Document();

 // Définissez une valeur pour la propriété de document intégrée « Titre ».
doc.BuiltInDocumentProperties.Title = "My Title";

// Nous pouvons utiliser le champ TITLE pour afficher la valeur de cette propriété dans le document.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Définition d'une valeur pour la propriété Texte du champ,
// et la mise à jour du champ écrasera également la propriété intégrée correspondante avec la nouvelle valeur.
builder.Writeln();
field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Text = "My New Title";
field.Update();

Assert.AreEqual(" TITLE  \"My New Title\"", field.GetFieldCode());
Assert.AreEqual("My New Title", field.Result);
Assert.AreEqual("My New Title", doc.BuiltInDocumentProperties.Title);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TITLE.docx");
```

### Voir également

* class [FieldTitle](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
