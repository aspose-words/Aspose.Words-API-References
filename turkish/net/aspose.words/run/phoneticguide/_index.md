---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: .NET için Aspose.Words
description: PhoneticGuide ile kusursuz telaffuzun kilidini açın. Kişiselleştirilmiş fonetik içgörülere erişerek dil becerilerinizi ve iletişiminizi geliştirin.
type: docs
weight: 40
url: /tr/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Bir tane alır`PhoneticGuide` nesne.

```csharp
public PhoneticGuide PhoneticGuide { get; }
```

## Örnekler

Fonetik rehberin özelliklerinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Asya metinlerinde fonetik kılavuzu kullanın.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### Ayrıca bakınız

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
