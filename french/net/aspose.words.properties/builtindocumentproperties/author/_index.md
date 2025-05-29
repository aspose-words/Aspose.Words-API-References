---
title: BuiltInDocumentProperties.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words pour .NET
description: Gérez facilement les auteurs de vos documents grâce à la propriété Auteur de BuiltInDocumentProperties. Définissez ou récupérez facilement le nom de l'auteur pour une meilleure organisation.
type: docs
weight: 10
url: /fr/net/aspose.words.properties/builtindocumentproperties/author/
---
## BuiltInDocumentProperties.Author property

Obtient ou définit le nom de l'auteur du document.

```csharp
public string Author { get; set; }
```

## Exemples

Montre comment travailler avec les propriétés de document intégrées dans la catégorie « Description ».

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Vous trouverez ci-dessous quatre propriétés de document intégrées qui ont des champs pouvant afficher leurs valeurs dans le corps du document.
// 1 - Propriété "Auteur", que nous pouvons afficher à l'aide d'un champ AUTEUR :
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - Propriété "Titre", que nous pouvons afficher à l'aide d'un champ TITLE :
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - Propriété "Sujet", que nous pouvons afficher à l'aide d'un champ SUBJECT :
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - Propriété "Commentaires", que nous pouvons afficher à l'aide d'un champ COMMENTAIRES :
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// La propriété intégrée « Catégorie » n'a pas de champ pouvant afficher sa valeur.
properties.Category = "My category";

// Nous pouvons définir plusieurs mots-clés pour un document en séparant la valeur de chaîne de la propriété « Mots-clés » par des points-virgules.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Nous pouvons faire un clic droit sur ce document dans l'Explorateur Windows et trouver ces propriétés dans "Propriétés" -> "Détails".
// La propriété intégrée « Auteur » se trouve dans le groupe « Origine » et les autres se trouvent dans le groupe « Description ».
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Voir également

* class [BuiltInDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
