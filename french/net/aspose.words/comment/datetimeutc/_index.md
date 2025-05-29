---
title: Comment.DateTimeUtc
linktitle: DateTimeUtc
articleTitle: DateTimeUtc
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Comment DateTimeUtc, qui récupère la date et l'heure UTC exactes de vos commentaires pour un suivi et une gestion précis.
type: docs
weight: 50
url: /fr/net/aspose.words/comment/datetimeutc/
---
## Comment.DateTimeUtc property

Obtient la date et l'heure UTC auxquelles le commentaire a été rédigé.

```csharp
public DateTime DateTimeUtc { get; }
```

## Remarques

La valeur par défaut est MinValue

## Exemples

Montre comment obtenir la date et l'heure UTC.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

DateTime dateTime = DateTime.Now;
Comment comment = new Comment(doc, "John Doe", "J.D.", dateTime);
comment.SetText("My comment.");

builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.UtcDateTime.docx");
doc = new Document(ArtifactsDir + "Comment.UtcDateTime.docx");

comment = (Comment)doc.GetChild(NodeType.Comment, 0, true);
// DateTimeUtc renvoie des données sans millisecondes.
Assert.AreEqual(dateTime.ToUniversalTime().ToString("yyyy-MM-dd hh:mm:ss"), comment.DateTimeUtc.ToString("yyyy-MM-dd hh:mm:ss"));
```

### Voir également

* class [Comment](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
