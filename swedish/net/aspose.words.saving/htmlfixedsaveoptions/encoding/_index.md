---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words för .NET
description: Upptäck kodningsegenskapen HtmlFixedSaveOptions för sömlös HTML-export. Ställ enkelt in UTF-8-kodning med BOM för optimal dataintegritet.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Anger vilken kodning som ska användas vid export till HTML. Standardvärdet är`ny UTF8-kodning(sant)` (UTF-8 med BOM).

```csharp
public Encoding Encoding { get; set; }
```

## Exempel

Visar hur man ställer in vilken kodning som ska användas vid export av ett dokument till HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// Standardkodningen är UTF-8. Om vi vill representera vårt dokument med en annan kodning,
// vi kan använda ett SaveOptions-objekt för att ställa in en specifik kodning.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
