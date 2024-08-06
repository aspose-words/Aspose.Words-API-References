---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words for .NET
description: Run IsPhoneticGuide property. Gets a boolean value indicating either the run is a phonetic guide in C#.
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
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### See Also

* class [Run](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
