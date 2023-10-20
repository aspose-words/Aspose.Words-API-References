---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words för .NET
description: Run PhoneticGuide fast egendom. Får enPhoneticGuide objekt i C#.
type: docs
weight: 40
url: /sv/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Får en`PhoneticGuide` objekt.

```csharp
public PhoneticGuide PhoneticGuide { get; }
```

## Exempel

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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
