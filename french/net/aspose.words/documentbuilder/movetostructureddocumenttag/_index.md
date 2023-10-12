---
title: DocumentBuilder.MoveToStructuredDocumentTag
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Déplace le curseur vers une balise de document structuré dans la section actuelle.
type: docs
weight: 590
url: /fr/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(int, int) {#movetostructureddocumenttag_1}

Déplace le curseur vers une balise de document structuré dans la section actuelle.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | L'index de la balise du document structuré vers laquelle se déplacer. |
| characterIndex | Int32 | L'index du caractère à l'intérieur de la balise du document structuré. Une valeur négative permet de spécifier une position à partir de la fin de la balise du document structuré. Utilisez -1 pour déplacer vers la fin de la balise du document structuré. Si la balise du document structuré est au niveau du bloc et que vous souhaitez déplacer le curseur à la fin de son dernier paragraphe, précisez -2. |

### Remarques

La navigation s'effectue à l'intérieur de l'histoire en cours de la section en cours. Autrement dit, si vous avez déplacé le curseur vers l'en-tête principal de la première section, alors*structuredDocumentTagIndex* a spécifié l'index de la balise du document structuré à l'intérieur de cet en-tête de cette section.

Quand*structuredDocumentTagIndex* est supérieur ou égal à 0, il spécifie un index dès le début de la section, 0 étant la première balise du document structuré. Quand *structuredDocumentTagIndex* est inférieur à 0, il a spécifié un index à partir de la fin de la section , -1 étant la dernière balise du document structuré.

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

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## MoveToStructuredDocumentTag(StructuredDocumentTag, int) {#movetostructureddocumenttag}

Déplace le curseur vers la balise du document structuré.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Balise du document structuré vers laquelle se déplacer. |
| characterIndex | Int32 | L'index du caractère à l'intérieur de la balise du document structuré. Une valeur négative permet de spécifier une position à partir de la fin de la balise du document structuré. Utilisez -1 pour déplacer vers la fin de la balise du document structuré. Si la balise du document structuré est au niveau du bloc et que vous souhaitez déplacer le curseur à la fin de son dernier paragraphe, précisez -2. |

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


