---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PhoneticGuide BaseText för att enkelt komma åt och förbättra fonetisk guidebastext för förbättrad tydlighet och kommunikation.
type: docs
weight: 10
url: /sv/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Hämtar bastexten för den fonetiska guiden.

```csharp
public string BaseText { get; }
```

## Exempel

Visar hur man hämtar egenskaper för den fonetiska guiden.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Använd fonetisk guide i den asiatiska texten.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### Se även

* class [PhoneticGuide](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
