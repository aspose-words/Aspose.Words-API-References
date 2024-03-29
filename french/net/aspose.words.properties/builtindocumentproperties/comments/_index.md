---
title: BuiltInDocumentProperties.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words pour .NET
description: BuiltInDocumentProperties Comments propriété. Obtient ou définit les commentaires du document en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.properties/builtindocumentproperties/comments/
---
## BuiltInDocumentProperties.Comments property

Obtient ou définit les commentaires du document.

```csharp
public string Comments { get; set; }
```

## Exemples

Montre comment utiliser les propriétés de document intégrées dans la catégorie « Description ».

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Vous trouverez ci-dessous quatre propriétés de document intégrées comportant des champs pouvant afficher leurs valeurs dans le corps du document.
// 1 - Propriété "Auteur", que l'on peut afficher à l'aide d'un champ AUTEUR :
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - Propriété "Titre", que l'on peut afficher à l'aide d'un champ TITRE :
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - Propriété "Sujet", que l'on peut afficher à l'aide d'un champ SUJET :
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - Propriété "Comments", que l'on peut afficher à l'aide d'un champ COMMENTS :
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// La propriété intégrée "Catégorie" n'a pas de champ pouvant afficher sa valeur.
properties.Category = "My category";

// Nous pouvons définir plusieurs mots-clés pour un document en séparant la valeur de chaîne de la propriété "Keywords" par des points-virgules.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Nous pouvons cliquer avec le bouton droit sur ce document dans l'Explorateur Windows et trouver ces propriétés dans "Propriétés" -> "Détails".
// La propriété intégrée "Auteur" est dans le groupe "Origine", et les autres sont dans le groupe "Description".
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Voir également

* class [BuiltInDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
