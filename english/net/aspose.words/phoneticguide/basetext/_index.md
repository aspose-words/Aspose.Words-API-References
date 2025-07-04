---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words for .NET
description: Discover the PhoneticGuide BaseText property to easily access and enhance phonetic guide base text for improved clarity and communication.
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
Assert.That(runs[0].IsPhoneticGuide, Is.EqualTo(true));
Assert.That(runs[0].PhoneticGuide.BaseText, Is.EqualTo("base"));
Assert.That(runs[0].PhoneticGuide.RubyText, Is.EqualTo("ruby"));
```

### See Also

* class [PhoneticGuide](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
