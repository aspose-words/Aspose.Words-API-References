---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words pour .NET
description: Découvrez IsPhoneticGuide, un outil puissant qui détermine si une exécution sert de guide phonétique, améliorant ainsi la clarté et la lisibilité de votre texte.
type: docs
weight: 20
url: /fr/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Obtient une valeur booléenne indiquant que l'exécution est un guide phonétique.

```csharp
public bool IsPhoneticGuide { get; }
```

## Exemples

Montre comment obtenir les propriétés du guide phonétique.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Utiliser le guide phonétique dans le texte asiatique.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### Voir également

* class [Run](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
