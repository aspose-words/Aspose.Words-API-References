---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words for .NET
description: Run PhoneticGuide property. Gets a PhoneticGuide object in C#.
type: docs
weight: 40
url: /net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Gets a `PhoneticGuide` object.

```csharp
public PhoneticGuide PhoneticGuide { get; }
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* namespace [Aspose.Words](../../run/)
* assembly [Aspose.Words](../../../)
