---
title: FileFormatInfo.Encoding
second_title: Aspose.Words für .NET-API-Referenz
description: FileFormatInfo eigendom. Ruft die erkannte Kodierung ab sofern diese auf das aktuelle Dokumentformat zutrifft. Erkennt derzeit nur die Kodierung für HTMLDokumente.
type: docs
weight: 10
url: /de/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Ruft die erkannte Kodierung ab, sofern diese auf das aktuelle Dokumentformat zutrifft. Erkennt derzeit nur die Kodierung für HTML-Dokumente.

```csharp
public Encoding Encoding { get; }
```

### Beispiele

Zeigt, wie die Codierung in einer HTML-Datei erkannt wird.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Die Encoding-Eigenschaft wird nur verwendet, wenn wir ein FileFormatInfo-Objekt für ein HTML-Dokument erstellen.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Siehe auch

* class [FileFormatInfo](../)
* namensraum [Aspose.Words](../../fileformatinfo/)
* Montage [Aspose.Words](../../../)


