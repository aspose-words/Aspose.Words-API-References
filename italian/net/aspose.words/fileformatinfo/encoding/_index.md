---
title: FileFormatInfo.Encoding
second_title: Aspose.Words per .NET API Reference
description: FileFormatInfo proprietà. Ottiene la codifica rilevata se applicabile al formato del documento corrente. Al momento rileva la codifica solo per i documenti HTML.
type: docs
weight: 10
url: /it/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Ottiene la codifica rilevata se applicabile al formato del documento corrente. Al momento rileva la codifica solo per i documenti HTML.

```csharp
public Encoding Encoding { get; }
```

### Esempi

Mostra come rilevare la codifica in un file html.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// La proprietà Encoding viene utilizzata solo quando creiamo un oggetto FileFormatInfo per un documento html.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Guarda anche

* class [FileFormatInfo](../)
* spazio dei nomi [Aspose.Words](../../fileformatinfo/)
* assemblea [Aspose.Words](../../../)


