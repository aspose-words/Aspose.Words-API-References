---
title: HtmlFixedSaveOptions.Encoding
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlFixedSaveOptions eigendom. Gibt die beim Exportieren in HTML zu verwendende Kodierung an. Der Standardwert istneue UTF8Encodingtrue UTF8 mit BOM.
type: docs
weight: 30
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Gibt die beim Exportieren in HTML zu verwendende Kodierung an. Der Standardwert ist`neue UTF8Encoding(true)` (UTF-8 mit BOM).

```csharp
public Encoding Encoding { get; set; }
```

### Beispiele

Zeigt, wie Sie festlegen, welche Codierung beim Exportieren eines Dokuments in HTML verwendet werden soll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// Die Standardcodierung ist UTF-8. Wenn wir unser Dokument mit einer anderen Codierung darstellen möchten,
// Wir können ein SaveOptions-Objekt verwenden, um eine bestimmte Codierung festzulegen.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.GetEncoding("ASCII")
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* Montage [Aspose.Words](../../../)


