---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
linktitle: IsAtEndOfStructuredDocumentTag
articleTitle: IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsAtEndOfStructuredDocumentTag de DocumentBuilder  vérifiez si votre curseur est positionné à la fin d'une balise de document structuré pour une édition efficace !
type: docs
weight: 120
url: /fr/net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

Retours**vrai** si le curseur se trouve à la fin d'une balise de document structuré.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
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

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
