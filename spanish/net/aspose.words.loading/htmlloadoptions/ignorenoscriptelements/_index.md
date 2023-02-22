---
title: HtmlLoadOptions.IgnoreNoscriptElements
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlLoadOptions propiedad. Obtiene o establece un valor que indica si se deben ignorar los elementos HTML noscript. El valor predeterminado esfalso .
type: docs
weight: 40
url: /es/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

Obtiene o establece un valor que indica si se deben ignorar los elementos HTML &lt;noscript&gt;. El valor predeterminado es`falso` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

### Observaciones

Al igual que MS Word, Aspose.Words no admite secuencias de comandos y, de forma predeterminada, carga contenido de &lt;noscript&gt; elementos en el documento resultante. En la mayoría de los navegadores, sin embargo, los scripts son compatibles y el contenido de &lt;noscript&gt; no es visible. Estableciendo esta propiedad en`verdadero` obliga a Aspose.Words a ignorar todos los elementos &lt;noscript&gt; y ayuda a producir documentos que se parecen más a lo que se ve en los navegadores.

### Ejemplos

Muestra cómo ignorar elementos HTML &lt;noscript&gt;.

```csharp
const string html = @"
    <html>
      <head>
        <title>NOSCRIPT</title>
          <meta http-equiv=""Content-Type"" content=""text/html; charset=utf-8"">
          <script type=""text/javascript"">
            alert(""Hello, world!"");
          </script>
      </head>
    <body>
      <noscript><p>Your browser does not support JavaScript!</p></noscript>
    </body>
    </html>";

HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
htmlLoadOptions.IgnoreNoscriptElements = ignoreNoscriptElements;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), htmlLoadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

### Ver también

* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../htmlloadoptions/)
* asamblea [Aspose.Words](../../../)


