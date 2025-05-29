---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words pour .NET
description: Découvrez comment améliorer la mise en page de votre texte grâce à la propriété Ponctuation suspendue de ParagraphFormat. Optimisez la lisibilité et le style sans effort !
type: docs
weight: 130
url: /fr/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Obtient ou définit un indicateur indiquant si la ponctuation suspendue est activée pour le paragraphe actuel.

```csharp
public bool HangingPunctuation { get; set; }
```

## Exemples

Montre comment définir des propriétés spéciales pour la typographie asiatique.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
