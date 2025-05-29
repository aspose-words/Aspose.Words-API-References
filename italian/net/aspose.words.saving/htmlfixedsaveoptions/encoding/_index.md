---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words per .NET
description: Scopri la proprietà di codifica HtmlFixedSaveOptions per esportazioni HTML fluide. Imposta facilmente la codifica UTF-8 con BOM per un'integrità ottimale dei dati.
type: docs
weight: 30
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Specifica la codifica da utilizzare durante l'esportazione in HTML. Il valore predefinito è`nuova codifica UTF8(vero)` (UTF-8 con BOM).

```csharp
public Encoding Encoding { get; set; }
```

## Esempi

Mostra come impostare la codifica da utilizzare durante l'esportazione di un documento in HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// La codifica predefinita è UTF-8. Se vogliamo rappresentare il nostro documento utilizzando una codifica diversa,
// possiamo usare un oggetto SaveOptions per impostare una codifica specifica.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
