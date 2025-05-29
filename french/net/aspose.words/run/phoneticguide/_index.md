---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words pour .NET
description: Bénéficiez d'une prononciation fluide avec PhoneticGuide. Améliorez vos compétences linguistiques et votre communication en accédant à des informations phonétiques personnalisées.
type: docs
weight: 40
url: /fr/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Obtient un`PhoneticGuide` objet.

```csharp
public PhoneticGuide PhoneticGuide { get; }
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
