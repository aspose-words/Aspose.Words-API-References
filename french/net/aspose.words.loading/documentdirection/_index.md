---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.DocumentDirection pour contrôler facilement le flux de texte dans vos documents. Améliorez la lisibilité et la mise en forme grâce à cette puissante fonctionnalité !
type: docs
weight: 4030
url: /fr/net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

Permet de spécifier la direction dans laquelle le texte doit circuler dans un document.

```csharp
public enum DocumentDirection
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| LeftToRight | `0` | Direction de gauche à droite. |
| RightToLeft | `1` | Direction de droite à gauche. |
| Auto | `2` | Détection automatique de la direction. |

## Exemples

Montre comment détecter la direction du texte d'un document en texte brut.

```csharp
// Créer un objet « TxtLoadOptions », que nous pouvons transmettre au constructeur d'un document
// pour modifier la façon dont nous chargeons un document en texte brut.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Définissez la propriété « DocumentDirection » sur « DocumentDirection.Auto » pour détecter automatiquement
// la direction de chaque paragraphe de texte qu'Aspose.Words charge à partir du texte brut.
// La propriété « Bidi » de chaque paragraphe stockera sa direction.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Détecter le texte hébreu comme étant de droite à gauche.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Détecter le texte anglais comme étant de droite à gauche.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Voir également

* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
