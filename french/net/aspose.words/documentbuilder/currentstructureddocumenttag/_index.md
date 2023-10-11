---
title: DocumentBuilder.CurrentStructuredDocumentTag
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder propriété. Obtient la balise de document structuré actuellement sélectionnée dans ceDocumentBuilder .
type: docs
weight: 80
url: /fr/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Obtient la balise de document structuré actuellement sélectionnée dans ce[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

### Exemples

Montre comment déplacer le curseur de DocumentBuilder à l'intérieur d'une balise de document structuré.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Il existe plusieurs manières de déplacer le curseur :
// 1 - Passer au premier caractère de la balise du document structuré par index.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Passer au premier caractère de la balise du document structuré par objet.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Passer à la fin de la deuxième balise du document structuré.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);            

// Récupère la balise du document structuré actuellement sélectionné.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Voir également

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


