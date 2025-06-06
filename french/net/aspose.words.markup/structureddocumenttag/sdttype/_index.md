---
title: StructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SdtType de StructuredDocumentTag pour identifier facilement les types de balises, améliorant ainsi la gestion et l'organisation de vos documents.
type: docs
weight: 250
url: /fr/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

Obtient le type de ceci**Balise de document structurée** .

```csharp
public SdtType SdtType { get; }
```

## Exemples

Montre comment obtenir le type d'une balise de document structuré.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### Voir également

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
