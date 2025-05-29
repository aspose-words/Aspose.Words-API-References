---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat FarEastLineBreakControl, qui permet d'utiliser des règles de saut de ligne d'Asie de l'Est pour une mise en forme précise du texte dans vos documents.
type: docs
weight: 110
url: /fr/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Obtient ou définit un indicateur indiquant si les règles de saut de ligne d'Asie de l'Est sont appliquées au paragraphe actuel.

```csharp
public bool FarEastLineBreakControl { get; set; }
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
