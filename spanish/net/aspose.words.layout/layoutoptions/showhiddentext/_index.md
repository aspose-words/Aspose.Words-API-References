---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: Aspose.Words para .NET
description: Descubre la propiedad ShowHiddenText de LayoutOptions y controla fácilmente la representación del texto oculto en tus documentos. ¡Optimiza la visibilidad de tu contenido hoy mismo!
type: docs
weight: 80
url: /es/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Obtiene o establece la indicación de si se representa el texto oculto en el documento. El valor predeterminado es`FALSO` .

```csharp
public bool ShowHiddenText { get; set; }
```

## Observaciones

Esta propiedad afecta a todo el contenido oculto, no solo al texto.

## Ejemplos

Muestra cómo ocultar texto en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Inserte texto oculto y luego especifique si deseamos omitirlo del documento renderizado.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Ver también

* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
