---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PhoneticGuide BaseText pour accéder facilement au texte de base du guide phonétique et l'améliorer pour une clarté et une communication améliorées.
type: docs
weight: 10
url: /fr/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Obtient le texte de base du guide phonétique.

```csharp
public string BaseText { get; }
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
