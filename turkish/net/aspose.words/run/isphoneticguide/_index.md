---
title: Run.IsPhoneticGuide
second_title: Aspose.Words for .NET API Referansı
description: Run mülk. Çalıştırmanın fonetik bir kılavuz olduğunu belirten bir boole değeri alır.
type: docs
weight: 20
url: /tr/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Çalıştırmanın fonetik bir kılavuz olduğunu belirten bir boole değeri alır.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* ad alanı [Aspose.Words](../../run/)
* toplantı [Aspose.Words](../../../)


