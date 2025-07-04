---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words for .NET
description: Discover IsPhoneticGuide, a powerful tool that determines if a run serves as a phonetic guide, enhancing your text's clarity and readability.
type: docs
weight: 20
url: /net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Gets a boolean value indicating either the run is a phonetic guide.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
