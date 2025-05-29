---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words för .NET
description: Upptäck IsPhoneticGuide, ett kraftfullt verktyg som avgör om en sändning fungerar som en fonetisk guide, vilket förbättrar din texts tydlighet och läsbarhet.
type: docs
weight: 20
url: /sv/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Hämtar ett booleskt värde som indikerar att körningen antingen är en fonetisk guide.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
