---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PhoneticGuide RubyText pour accéder et améliorer le texte Ruby pour une meilleure clarté phonétique dans vos applications.
type: docs
weight: 20
url: /fr/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Obtient le texte Ruby du guide phonétique.

```csharp
public string RubyText { get; }
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

* class [PhoneticGuide](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
