---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété IsFormatRevision dans Microsoft Word suit les modifications de mise en forme, garantissant des modifications de documents précises et une collaboration améliorée.
type: docs
weight: 90
url: /fr/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Renvoie true si la mise en forme de l'objet a été modifiée dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsFormatRevision { get; }
```

## Exemples

Montre comment vérifier si un paragraphe est une révision de format.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Ce paragraphe est une révision de « Format », qui se produit lorsque nous modifions la mise en forme d'un texte existant
// lors du suivi des révisions dans Microsoft Word via « Révision » -> « Suivre les modifications ».
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
