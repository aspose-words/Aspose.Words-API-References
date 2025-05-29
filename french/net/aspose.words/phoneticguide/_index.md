---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.PhoneticGuide pour améliorer la lisibilité du texte grâce aux guides phonétiques. Améliorez l'expérience utilisateur et l'accessibilité sans effort !
type: docs
weight: 5160
url: /fr/net/aspose.words/phoneticguide/
---
## PhoneticGuide class

Représente le guide phonétique.

```csharp
public class PhoneticGuide
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | Obtient le texte de base du guide phonétique. |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | Obtient le texte Ruby du guide phonétique. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
