---
title: FieldAuthor.AuthorName
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldAuthor propriété. Obtient ou définit le nom de lauteur du document.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldauthor/authorname/
---
## FieldAuthor.AuthorName property

Obtient ou définit le nom de l'auteur du document.

```csharp
public string AuthorName { get; set; }
```

### Exemples

Montre comment utiliser un champ AUTEUR pour afficher le nom du créateur d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les champs AUTHOR tirent leurs résultats de la propriété de document intégrée appelée "Auteur".
// Si nous créons et enregistrons un document dans Microsoft Word,
// il aura notre nom d'utilisateur dans cette propriété.
// Cependant, si nous créons un document par programme en utilisant Aspose.Words,
 // la propriété "Auteur", par défaut, sera une chaîne vide.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Définir un nom d'auteur de sauvegarde pour les champs AUTEUR à utiliser
// si la propriété "Auteur" contient une chaîne vide.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Mise à jour d'un champ AUTEUR contenant une valeur
// appliquera cette valeur à la propriété intégrée "Auteur".
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Changer cette propriété, puis mettre à jour le champ AUTEUR appliquera cette valeur au champ.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Si on met à jour un champ AUTHOR après avoir changé sa propriété "Name",
// alors le champ affichera le nouveau nom et appliquera le nouveau nom à la propriété intégrée.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// Les champs AUTHOR n'affectent pas la propriété DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Voir également

* class [FieldAuthor](../)
* espace de noms [Aspose.Words.Fields](../../fieldauthor/)
* Assemblée [Aspose.Words](../../../)


