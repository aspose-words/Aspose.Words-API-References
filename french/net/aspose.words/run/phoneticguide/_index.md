---
title: Run.PhoneticGuide
second_title: Référence de l'API Aspose.Words pour .NET
description: Run propriété. Obtient unPhoneticGuide objet.
type: docs
weight: 40
url: /fr/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Obtient un`PhoneticGuide` objet.

```csharp
public PhoneticGuide PhoneticGuide { get; }
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* espace de noms [Aspose.Words](../../run/)
* Assemblée [Aspose.Words](../../../)


