---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words for .NET
description: PhoneticGuide BaseText mülk. Fonetik kılavuzun temel metnini alır C#'da.
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

* class [PhoneticGuide](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
