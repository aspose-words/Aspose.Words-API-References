---
title: IStructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SdtType IStructuredDocumentTag pour identifier facilement le type de balises de document structuré pour une gestion améliorée des documents.
type: docs
weight: 120
url: /fr/net/aspose.words.markup/istructureddocumenttag/sdttype/
---
## IStructuredDocumentTag.SdtType property

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
* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
