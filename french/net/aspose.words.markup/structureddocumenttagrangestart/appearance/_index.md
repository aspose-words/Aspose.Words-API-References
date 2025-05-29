---
title: StructuredDocumentTagRangeStart.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words pour .NET
description: Découvrez comment personnaliser l'apparence de StructuredDocumentTagRangeStart pour une mise en forme améliorée du document et une meilleure lisibilité.
type: docs
weight: 20
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/appearance/
---
## StructuredDocumentTagRangeStart.Appearance property

Obtient ou définit l'apparence de la balise de document structuré.

```csharp
public SdtAppearance Appearance { get; set; }
```

## Exemples

Montre comment afficher les balises autour du contenu.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### Voir également

* enum [SdtAppearance](../../sdtappearance/)
* class [StructuredDocumentTagRangeStart](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
