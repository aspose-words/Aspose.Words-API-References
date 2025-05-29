---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Markup.SdtAppearance pour personnaliser l'apparence des balises de documents structurés. Améliorez la mise en forme de vos documents sans effort !
type: docs
weight: 4680
url: /fr/net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

Spécifie l'apparence d'une balise de document structuré.

```csharp
public enum SdtAppearance
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| BoundingBox | `0` | Représente une balise de document structurée affichée sous la forme d'un rectangle ombré ou d'un cadre englobant. |
| Tags | `1` | Représente une balise de document structurée affichée sous forme de marqueurs de début et de fin. |
| Hidden | `2` | Représente une balise de document structurée qui n'est pas affichée. |
| Default | `0` | Par défautBoundingBox . |

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

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
