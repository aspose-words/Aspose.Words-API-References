---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: .NET için Aspose.Words
description: Fonetik rehber temel metnine kolayca erişmek ve onu geliştirerek daha iyi bir netlik ve iletişim sağlamak için PhoneticGuide BaseText özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Fonetik kılavuzun temel metnini alır.

```csharp
public string BaseText { get; }
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

* class [PhoneticGuide](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
