---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ParagraphFormat WordWrap affecte l'habillage du texte dans Word. Apprenez à contrôler le flux de texte latin pour une meilleure lisibilité des documents.
type: docs
weight: 420
url: /fr/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Si cette propriété est`FAUX` Le texte latin au milieu d'un mot peut être encapsulé pour le paragraphe actuel. Sinon, le texte latin est encapsulé par des mots entiers.

```csharp
public bool WordWrap { get; set; }
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
