---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words für .NET
description: Entdecken Sie die HtmlFixedSaveOptions-Kodierungseigenschaft für nahtlose HTML-Exporte. Stellen Sie die UTF-8-Kodierung mit BOM einfach ein, um optimale Datenintegrität zu gewährleisten.
type: docs
weight: 30
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Gibt die Kodierung an, die beim Exportieren nach HTML verwendet werden soll. Der Standardwert ist`neue UTF8-Kodierung (true)` (UTF-8 mit BOM).

```csharp
public Encoding Encoding { get; set; }
```

## Beispiele

Zeigt, wie Sie beim Exportieren eines Dokuments in HTML festlegen, welche Kodierung verwendet werden soll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// Die Standardkodierung ist UTF-8. Wenn wir unser Dokument mit einer anderen Kodierung darstellen möchten,
// Wir können ein SaveOptions-Objekt verwenden, um eine bestimmte Kodierung festzulegen.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
