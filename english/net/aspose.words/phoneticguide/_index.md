---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.PhoneticGuide class for enhancing text readability with phonetic guides. Improve user experience and accessibility effortlessly!
type: docs
weight: 5020
url: /net/aspose.words/phoneticguide/
---
## PhoneticGuide class

Represents Phonetic Guide.

```csharp
public class PhoneticGuide
```

## Properties

| Name | Description |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | Gets base text of the phonetic guide. |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | Gets ruby text of the phonetic guide. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
