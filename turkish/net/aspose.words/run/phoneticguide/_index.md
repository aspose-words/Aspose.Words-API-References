---
title: Run.PhoneticGuide
second_title: Aspose.Words for .NET API Referansı
description: Run mülk. Bir alırPhoneticGuide nesne.
type: docs
weight: 40
url: /tr/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Bir alır`PhoneticGuide` nesne.

```csharp
public PhoneticGuide PhoneticGuide { get; }
```

### Örnekler

Fonetik kılavuzun özelliklerinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Asya metninde fonetik kılavuzu kullanın.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Ayrıca bakınız

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* ad alanı [Aspose.Words](../../run/)
* toplantı [Aspose.Words](../../../)


