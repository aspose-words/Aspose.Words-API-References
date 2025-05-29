---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: Aspose.Words pour .NET
description: Gérez la propriété DefaultDocumentAuthor pour définir ou mettre à jour facilement les noms des auteurs de documents, améliorant ainsi l'organisation et l'efficacité de la gestion des documents.
type: docs
weight: 70
url: /fr/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

Récupère ou définit le nom de l'auteur par défaut du document. Si le nom de l'auteur est déjà spécifié dans les propriétés intégrées du document, cette option n'est pas prise en compte.

```csharp
public string DefaultDocumentAuthor { get; set; }
```

## Exemples

Montre comment utiliser un champ AUTEUR pour afficher le nom du créateur d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les champs AUTEUR tirent leurs résultats de la propriété de document intégrée appelée « Auteur ».
// Si nous créons et enregistrons un document dans Microsoft Word,
// il aura notre nom d'utilisateur dans cette propriété.
// Cependant, si nous créons un document par programmation en utilisant Aspose.Words,
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
// appliquera cette valeur à la propriété intégrée « Auteur ».
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// La modification de cette propriété, puis la mise à jour du champ AUTEUR appliqueront cette valeur au champ.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Si nous mettons à jour un champ AUTEUR après avoir modifié sa propriété « Nom »,
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

* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
