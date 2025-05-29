---
title: IStructuredDocumentTag.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Apparence IStructuredDocumentTag pour personnaliser et améliorer vos balises de documents structurés pour une meilleure expérience utilisateur.
type: docs
weight: 10
url: /fr/net/aspose.words.markup/istructureddocumenttag/appearance/
---
## IStructuredDocumentTag.Appearance property

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
* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
