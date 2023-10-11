---
title: PhoneticGuide.BaseText
second_title: Référence de l'API Aspose.Words pour .NET
description: PhoneticGuide propriété. Obtient le texte de base du guide phonétique.
type: docs
weight: 10
url: /fr/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Obtient le texte de base du guide phonétique.

```csharp
public string BaseText { get; }
```

### Exemples

Montre comment obtenir les propriétés du guide phonétique.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Utiliser un guide phonétique dans le texte asiatique.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Voir également

* class [PhoneticGuide](../)
* espace de noms [Aspose.Words](../../phoneticguide/)
* Assemblée [Aspose.Words](../../../)


