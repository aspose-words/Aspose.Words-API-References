---
title: PhoneticGuide.BaseText
second_title: Aspose.Words för .NET API Referens
description: PhoneticGuide fast egendom. Hämtar bastext för den fonetiska guiden.
type: docs
weight: 10
url: /sv/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Hämtar bastext för den fonetiska guiden.

```csharp
public string BaseText { get; }
```

### Exempel

Visar hur man får egenskaper för den fonetiska guiden.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Använd fonetisk guide i den asiatiska texten.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Se även

* class [PhoneticGuide](../)
* namnutrymme [Aspose.Words](../../phoneticguide/)
* hopsättning [Aspose.Words](../../../)


