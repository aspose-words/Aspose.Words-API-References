---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words för .NET
description: Få tillgång till sömlöst uttal med PhoneticGuide. Förbättra dina språkkunskaper och din kommunikation genom att få tillgång till personliga fonetiska insikter.
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
