---
title: Run.IsPhoneticGuide
second_title: Aspose.Words för .NET API Referens
description: Run fast egendom. Får ett booleskt värde som anger att antingen körningen är en fonetisk guide.
type: docs
weight: 20
url: /sv/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Får ett booleskt värde som anger att antingen körningen är en fonetisk guide.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* namnutrymme [Aspose.Words](../../run/)
* hopsättning [Aspose.Words](../../../)


