---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.PdfPageLayout pour une visualisation optimale des PDF. Personnalisez la mise en page pour une meilleure lisibilité dans n'importe quel lecteur PDF.
type: docs
weight: 6290
url: /fr/net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

Spécifie la mise en page à utiliser lorsque le document est ouvert dans un lecteur PDF.

```csharp
public enum PdfPageLayout
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| SinglePage | `0` | Afficher une page à la fois. |
| OneColumn | `1` | Afficher les pages dans une colonne. |
| TwoColumnLeft | `2` | Affichez les pages sur deux colonnes, avec les pages impaires à gauche. |
| TwoColumnRight | `3` | Affichez les pages sur deux colonnes, avec les pages impaires à droite. |
| TwoPageLeft | `4` | Affichez les pages deux par deux, avec les pages impaires à gauche. |
| TwoPageRight | `5` | Affichez les pages deux par deux, avec les pages impaires à droite. |

## Exemples

Montre comment afficher les pages lorsqu'elles sont ouvertes dans un lecteur PDF.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Affichez les pages deux par deux, avec les pages impaires à gauche.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
