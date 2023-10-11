---
title: HtmlFixedSaveOptions.Encoding
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlFixedSaveOptions propiedad. Especifica la codificación que se utilizará al exportar a HTML. El valor predeterminado esnueva codificación UTF8 verdadero UTF8 con lista de materiales.
type: docs
weight: 30
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Especifica la codificación que se utilizará al exportar a HTML. El valor predeterminado es`nueva codificación UTF8 (verdadero)` (UTF-8 con lista de materiales).

```csharp
public Encoding Encoding { get; set; }
```

### Ejemplos

Muestra cómo configurar qué codificación usar al exportar un documento a HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// La codificación predeterminada es UTF-8. Si queremos representar nuestro documento usando una codificación diferente,
// podemos usar un objeto SaveOptions para establecer una codificación específica.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.GetEncoding("ASCII")
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* asamblea [Aspose.Words](../../../)


