---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words pour .NET
description: Découvrez la fonction Souligner de DocumentBuilder pour personnaliser facilement les styles de police. Améliorez vos documents grâce à des options de soulignement polyvalentes pour un rendu professionnel.
type: docs
weight: 190
url: /fr/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Obtient/définit le type de soulignement pour la police actuelle.

```csharp
public Underline Underline { get; set; }
```

## Exemples

Montre comment formater le texte inséré par un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// Le générateur applique la mise en forme à son paragraphe actuel et à tout nouveau texte ajouté par la suite.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Voir également

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
