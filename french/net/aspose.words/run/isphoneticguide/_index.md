---
title: Run.IsPhoneticGuide
second_title: Référence de l'API Aspose.Words pour .NET
description: Run propriété. Obtient une valeur booléenne indiquant que lexécution est un guide phonétique.
type: docs
weight: 20
url: /fr/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Obtient une valeur booléenne indiquant que l'exécution est un guide phonétique.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* espace de noms [Aspose.Words](../../run/)
* Assemblée [Aspose.Words](../../../)


