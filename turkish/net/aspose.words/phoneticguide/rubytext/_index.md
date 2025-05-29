---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: .NET için Aspose.Words
description: Uygulamalarınızda fonetik netliği artırmak için ruby metnine erişmek ve onu geliştirmek amacıyla PhoneticGuide RubyText özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Fonetik kılavuzun yakut metnini alır.

```csharp
public string RubyText { get; }
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
