---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: Aspose.Words pour .NET
description: Améliorez vos documents sans effort grâce à la méthode InsertStructuredDocumentTag de DocumentBuilder. Ajoutez facilement des balises structurées pour une meilleure organisation !
type: docs
weight: 480
url: /fr/net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

Insère un[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) dans le document.

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### Return_Value

Le[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) nœud qui vient d'être inséré.

## Exemples

Montre comment insérer simplement une balise de document structurée.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// Notez que seuls les types StructuredDocumentTag suivants sont autorisés pour l'insertion :
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Image, SdtType.Date.
// Le niveau de balisage du StructuredDocumentTag inséré sera détecté automatiquement et dépend de la position à laquelle il est inséré.
// L'ajout de StructuredDocumentTag héritera du formatage des paragraphes et des polices de la position du curseur.
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### Voir également

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
