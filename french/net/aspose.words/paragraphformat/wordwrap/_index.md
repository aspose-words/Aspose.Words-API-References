---
title: WordWrap
second_title: Référence de l'API Aspose.Words pour .NET
description: Si cette propriété est faux le texte latin au milieu dun mot peut être enveloppé for le paragraphe en cours. Sinon le texte latin est entouré de mots entiers.
type: docs
weight: 400
url: /fr/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Si cette propriété est **faux** le texte latin au milieu d'un mot peut être enveloppé for le paragraphe en cours. Sinon, le texte latin est entouré de mots entiers.

```csharp
public bool WordWrap { get; set; }
```

### Exemples

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

* class [ParagraphFormat](../../paragraphformat)
* espace de noms [Aspose.Words](../../paragraphformat)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->