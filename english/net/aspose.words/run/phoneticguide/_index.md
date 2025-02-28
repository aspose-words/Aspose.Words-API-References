---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words for .NET
description: Unlock seamless pronunciation with PhoneticGuide. Enhance your language skills and communication by accessing personalized phonetic insights.
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

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### See Also

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
