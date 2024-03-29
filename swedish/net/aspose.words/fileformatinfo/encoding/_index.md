---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words för .NET
description: FileFormatInfo Encoding fast egendom. Hämtar den upptäckta kodningen om det är tillämpligt för det aktuella dokumentformatet. Detekterar för närvarande kodning endast för HTMLdokument i C#.
type: docs
weight: 10
url: /sv/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Hämtar den upptäckta kodningen om det är tillämpligt för det aktuella dokumentformatet. Detekterar för närvarande kodning endast för HTML-dokument.

```csharp
public Encoding Encoding { get; }
```

## Exempel

Visar hur man upptäcker kodning i en html-fil.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Encoding-egenskapen används endast när vi skapar ett FileFormatInfo-objekt för ett HTML-dokument.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Se även

* class [FileFormatInfo](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
