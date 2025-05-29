---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words pour .NET
description: Naviguez sans effort vers les balises de documents structurés avec la méthode MoveToStructuredDocumentTag de DocumentBuilder, améliorant ainsi l'efficacité de l'édition de vos documents.
type: docs
weight: 620
url: /fr/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

Déplace le curseur vers une balise de document structuré dans la section actuelle.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | L'index de la balise de document structuré vers laquelle se déplacer. |
| characterIndex | Int32 | Index du caractère à l'intérieur de la balise de document structuré. Une valeur négative permet de spécifier une position à partir de la fin de la balise de document structuré. Utilisez -1 pour vous déplacer à la fin de la balise de document structuré. Si la balise de document structuré est au niveau du bloc et que vous souhaitez déplacer le curseur à la fin de son dernier paragraphe, spécifiez -2. |

## Remarques

La navigation s'effectue à l'intérieur de l'article courant de la section courante. Autrement dit, si vous déplacez le curseur sur l'en-tête principal de la première section,*structuredDocumentTagIndex* a spécifié l'index de la balise de document structuré à l'intérieur de cet en-tête de cette section.

Quand*structuredDocumentTagIndex* Si la valeur est supérieure ou égale à 0, elle spécifie un index à partir du début de la section, 0 étant la première balise de document structuré.*structuredDocumentTagIndex*est inférieur à 0, il a spécifié un index à partir de la fin de la section avec -1 étant la dernière balise de document structuré.

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

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

Déplace le curseur vers la balise du document structuré.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | La balise de document structuré vers laquelle se déplacer. |
| characterIndex | Int32 | Index du caractère à l'intérieur de la balise de document structuré. Une valeur négative permet de spécifier une position à partir de la fin de la balise de document structuré. Utilisez -1 pour vous déplacer à la fin de la balise de document structuré. Si la balise de document structuré est au niveau du bloc et que vous souhaitez déplacer le curseur à la fin de son dernier paragraphe, spécifiez -2. |

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
