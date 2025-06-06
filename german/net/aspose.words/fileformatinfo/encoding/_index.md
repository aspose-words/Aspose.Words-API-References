---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words für .NET
description: Entdecken Sie die FileFormatInfo-Kodierungseigenschaft, um die Dokumentkodierung mühelos zu identifizieren. Unterstützt aktuell HTML-Formate für präzise Ergebnisse.
type: docs
weight: 10
url: /de/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Ruft die erkannte Kodierung ab, sofern sie auf das aktuelle Dokumentformat anwendbar ist. Derzeit wird die Kodierung nur für HTML-Dokumente erkannt.

```csharp
public Encoding Encoding { get; }
```

## Beispiele

Zeigt, wie die Kodierung in einer HTML-Datei erkannt wird.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Die Encoding-Eigenschaft wird nur verwendet, wenn wir ein FileFormatInfo-Objekt für ein HTML-Dokument erstellen.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Siehe auch

* class [FileFormatInfo](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
