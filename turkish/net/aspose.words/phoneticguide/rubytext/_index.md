---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words for .NET
description: PhoneticGuide RubyText mülk. Fonetik kılavuzun ruby metnini alır C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Fonetik kılavuzun ruby metnini alır.

```csharp
public string RubyText { get; }
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
