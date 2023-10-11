---
title: PageSetup.TextOrientation
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Permite especificarTextOrientation para toda la página. El valor predeterminado esHorizontal
type: docs
weight: 430
url: /es/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Permite especificar`TextOrientation` para toda la página. El valor predeterminado esHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

### Observaciones

Esta propiedad sólo es compatible con los formatos nativos de MS Word DOCX, WML, RTF y DOC.

### Ejemplos

Muestra cómo configurar la orientación del texto.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Establece la propiedad "TextOrientation" en "TextOrientation.Upward" para rotar todo el texto 90 grados
// a la derecha para que todo el texto de izquierda a derecha vaya ahora de arriba a abajo.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Ver también

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


