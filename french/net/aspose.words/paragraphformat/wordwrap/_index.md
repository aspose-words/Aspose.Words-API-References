---
title: ParagraphFormat.WordWrap
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Si cette propriété estFAUX  le texte latin au milieu dun mot peut être renvoyé à la ligne pour le paragraphe actuel. Sinon le texte latin est entouré de mots entiers.
type: docs
weight: 410
url: /fr/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Si cette propriété est`FAUX` , le texte latin au milieu d'un mot peut être renvoyé à la ligne pour le paragraphe actuel. Sinon, le texte latin est entouré de mots entiers.

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

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


