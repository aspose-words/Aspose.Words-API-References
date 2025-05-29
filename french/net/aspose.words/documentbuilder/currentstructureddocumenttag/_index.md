---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words pour .NET
description: Découvrez la propriété CurrentStructuredDocumentTag dans DocumentBuilder. Accédez facilement à la balise de document structuré sélectionnée pour une gestion documentaire efficace.
type: docs
weight: 80
url: /fr/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Obtient la balise de document structuré actuellement sélectionnée dans ce[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## Exemples

Montre comment déplacer le curseur de DocumentBuilder à l'intérieur d'une balise de document structurée.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Il existe plusieurs façons de déplacer le curseur :
// 1 - Déplacer vers le premier caractère de la balise de document structuré par index.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Déplacer vers le premier caractère de la balise de document structuré par objet.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Déplacer vers la fin de la deuxième balise de document structuré.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// Obtenir la balise de document structuré actuellement sélectionnée.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Voir également

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
