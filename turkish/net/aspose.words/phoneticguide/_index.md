---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: .NET için Aspose.Words
description: Fonetik kılavuzlarla metin okunabilirliğini geliştirmek için Aspose.Words.PhoneticGuide sınıfını keşfedin. Kullanıcı deneyimini ve erişilebilirliği zahmetsizce geliştirin!
type: docs
weight: 5160
url: /tr/net/aspose.words/phoneticguide/
---
## PhoneticGuide class

Fonetik Kılavuzu temsil eder.

```csharp
public class PhoneticGuide
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | Fonetik kılavuzun temel metnini alır. |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | Fonetik kılavuzun yakut metnini alır. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
