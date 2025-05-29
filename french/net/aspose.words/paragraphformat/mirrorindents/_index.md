---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ParagraphFormat MirrorIndents améliore la mise en forme de votre document en garantissant des retraits gauche et droit cohérents pour un aspect soigné.
type: docs
weight: 240
url: /fr/net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

Obtient ou définit un indicateur indiquant si les retraits gauche et droit ont la même largeur.

```csharp
public bool MirrorIndents { get; set; }
```

## Exemples

Montrez comment rendre les retraits à gauche et à droite identiques.

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
