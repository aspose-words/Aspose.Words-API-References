---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words for .NET
description: Run IsPhoneticGuide mülk. Çalıştırmanın fonetik bir kılavuz olduğunu belirten bir boole değeri alır C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Çalıştırmanın fonetik bir kılavuz olduğunu belirten bir boole değeri alır.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
