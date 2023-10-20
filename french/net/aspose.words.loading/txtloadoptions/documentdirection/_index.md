---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words pour .NET
description: TxtLoadOptions DocumentDirection propriété. Obtient ou définit une direction de document. La valeur par défaut estLeftToRight  en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Obtient ou définit une direction de document. La valeur par défaut estLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## Exemples

Montre comment détecter la direction du texte d'un document en texte brut.

```csharp
// Crée un objet "TxtLoadOptions", que l'on peut transmettre au constructeur d'un document
// pour modifier la façon dont nous chargeons un document en texte brut.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Définissez la propriété "DocumentDirection" sur "DocumentDirection.Auto" détecte automatiquement
// la direction de chaque paragraphe de texte chargé par Aspose.Words à partir du texte brut.
// La propriété "Bidi" de chaque paragraphe stockera sa direction.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Détecte le texte hébreu de droite à gauche.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Détecte le texte anglais de droite à gauche.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Voir également

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
