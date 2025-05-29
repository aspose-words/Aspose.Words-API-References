---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words para .NET
description: Descubre la propiedad PageSetup TextOrientation para configurar fácilmente la dirección del texto de la página. Personaliza tu diseño con opciones que van más allá de la opción predeterminada "Horizontal".
type: docs
weight: 430
url: /es/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Permite especificar`TextOrientation` para toda la página. El valor predeterminado esHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Observaciones

Esta propiedad solo es compatible con los formatos nativos de MS Word DOCX, WML, RTF y DOC.

## Ejemplos

Muestra cómo establecer la orientación del texto.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Establezca la propiedad "TextOrientation" en "TextOrientation.Upward" para rotar todo el texto 90 grados
// hacia la derecha para que todo el texto de izquierda a derecha ahora vaya de arriba hacia abajo.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Ver también

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
