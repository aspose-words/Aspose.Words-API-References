---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.PhoneticGuide för att förbättra textläsbarheten med fonetiska guider. Förbättra användarupplevelsen och tillgängligheten utan ansträngning!
type: docs
weight: 5160
url: /sv/net/aspose.words/phoneticguide/
---
## PhoneticGuide class

Representerar fonetisk guide.

```csharp
public class PhoneticGuide
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | Hämtar bastexten för den fonetiska guiden. |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | Hämtar rubinröd text från den fonetiska guiden. |

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
