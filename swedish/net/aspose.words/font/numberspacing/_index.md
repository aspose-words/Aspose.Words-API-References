---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font NumberSpacing för att anpassa sifferavståndet för förbättrad läsbarhet och design. Optimera din typografi idag!
type: docs
weight: 290
url: /sv/net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

Hämtar eller ställer in avståndstypen för den siffra som visas.

```csharp
public NumSpacing NumberSpacing { get; set; }
```

## Exempel

Visar hur man ställer in avståndstypen för siffran.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Den här effekten stöds endast i nyare versioner av MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Se även

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
