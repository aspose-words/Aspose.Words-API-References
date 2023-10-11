---
title: Paragraph.IsFormatRevision
second_title: Référence de l'API Aspose.Words pour .NET
description: Paragraph propriété. Renvoie vrai si le formatage de lobjet a été modifié dans Microsoft Word alors que le suivi des modifications était activé.
type: docs
weight: 90
url: /fr/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Renvoie vrai si le formatage de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsFormatRevision { get; }
```

### Exemples

Montre comment vérifier si un paragraphe est une révision de format.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Ce paragraphe est une révision "Format", qui se produit lorsque nous modifions le formatage du texte existant
// lors du suivi des révisions dans Microsoft Word via "Review" -> "Suivi des modifications".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)


