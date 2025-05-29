---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.TextWatermarkOptions para marcas de agua de texto personalizables. ¡Mejore sus documentos con opciones de marca únicas y profesionales!
type: docs
weight: 7290
url: /es/net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

Contiene opciones que se pueden especificar al agregar una marca de agua con texto.

Para obtener más información, visite el[Trabajar con marca de agua](https://docs.aspose.com/words/net/working-with-watermark/) Artículo de documentación.

```csharp
public class TextWatermarkOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | Obtiene o establece el color de la fuente. El valor predeterminado esSilver . |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | Obtiene o establece el nombre de la familia de fuentes. El valor predeterminado es "Calibri". |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | Obtiene o establece el tamaño de fuente. El valor predeterminado es 0 - auto. |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | Obtiene o establece un valor booleano que es responsable de la opacidad de la marca de agua. El valor predeterminado es`verdadero` . |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | Obtiene o establece el diseño de la marca de agua. El valor predeterminado esDiagonal . |

## Ejemplos

Muestra cómo crear una marca de agua de texto.

```csharp
Document doc = new Document();

//Agrega una marca de agua de texto simple.
doc.Watermark.SetText("Aspose Watermark");

// Si deseamos editar el formato del texto usándolo como marca de agua,
// Podemos hacerlo pasando un objeto TextWatermarkOptions al crear la marca de agua.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

//Podemos eliminar una marca de agua de un documento como este.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
