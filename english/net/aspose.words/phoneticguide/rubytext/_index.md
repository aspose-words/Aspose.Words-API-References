---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words for .NET
description: Discover the PhoneticGuide RubyText property to access and enhance ruby text for improved phonetic clarity in your applications.
type: docs
weight: 20
url: /net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Gets ruby text of the phonetic guide.

```csharp
public string RubyText { get; }
```

## Examples

Shows how to get properties of the phonetic guide.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Use phonetic guide in the Asian text.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### See Also

* class [PhoneticGuide](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
