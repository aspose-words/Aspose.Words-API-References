---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words for .NET
description: PhoneticGuide BaseText property. Gets base text of the phonetic guide in C#.
type: docs
weight: 10
url: /net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Gets base text of the phonetic guide.

```csharp
public string BaseText { get; }
```

## Examples

Shows how to get properties of the phonetic guide.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Use phonetic guide in the Asian text.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### See Also

* class [PhoneticGuide](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
