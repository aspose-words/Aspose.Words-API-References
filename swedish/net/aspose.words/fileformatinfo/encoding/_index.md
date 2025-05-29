---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FileFormatInfo Encoding för att enkelt identifiera dokumentkodning. Stöder för närvarande HTML-format för korrekta resultat.
type: docs
weight: 10
url: /sv/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Hämtar den detekterade kodningen om den är tillämplig för det aktuella dokumentformatet. För närvarande identifieras kodning endast för HTML-dokument.

```csharp
public Encoding Encoding { get; }
```

## Exempel

Visar hur man identifierar kodning i en html-fil.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Egenskapen Encoding används endast när vi skapar ett FileFormatInfo-objekt för ett HTML-dokument.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Se även

* class [FileFormatInfo](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
