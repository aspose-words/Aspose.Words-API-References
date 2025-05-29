---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words para .NET
description: Descubra la propiedad de codificación HtmlFixedSaveOptions para una exportación HTML fluida. Configure fácilmente la codificación UTF-8 con BOM para una integridad de datos óptima.
type: docs
weight: 30
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Especifica la codificación que se utilizará al exportar a HTML. El valor predeterminado es`nueva codificación UTF8 (verdadero)` (UTF-8 con BOM).

```csharp
public Encoding Encoding { get; set; }
```

## Ejemplos

Muestra cómo configurar la codificación a utilizar al exportar un documento a HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

La codificación predeterminada es UTF-8. Si queremos representar nuestro documento con una codificación diferente,
//podemos usar un objeto SaveOptions para establecer una codificación específica.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
