---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PhoneticGuide RubyText för att få åtkomst till och förbättra Ruby-text för förbättrad fonetisk tydlighet i dina applikationer.
type: docs
weight: 20
url: /sv/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Hämtar rubinröd text från den fonetiska guiden.

```csharp
public string RubyText { get; }
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
