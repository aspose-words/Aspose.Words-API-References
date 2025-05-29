---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: .NET için Aspose.Words
description: Metninizin netliğini ve okunabilirliğini artırarak, bir koşunun fonetik rehber olarak kullanılıp kullanılmadığını belirleyen güçlü bir araç olan IsPhoneticGuide'ı keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Çalışmanın fonetik bir kılavuz olup olmadığını belirten bir Boole değeri alır.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
