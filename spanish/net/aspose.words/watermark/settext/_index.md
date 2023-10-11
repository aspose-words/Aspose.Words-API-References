---
title: Watermark.SetText
second_title: Referencia de API de Aspose.Words para .NET
description: Watermark método. Agrega una marca de agua de texto al documento.
type: docs
weight: 40
url: /es/net/aspose.words/watermark/settext/
---
## SetText(string) {#settext}

Agrega una marca de agua de texto al documento.

```csharp
public void SetText(string text)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| text | String | Texto que se muestra como una marca de agua. |

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza cuando la longitud del texto está fuera de rango o el texto contiene solo espacios en blanco. |
| ArgumentNullException | Se lanza cuando el texto es`nulo` . |

### Observaciones

La longitud del texto debe estar en el rango de 1 a 200 inclusive. El texto no puede`nulo` o contener solo espacios en blanco.

### Ejemplos

Muestra cómo crear una marca de agua de texto.

```csharp
Document doc = new Document();

// Agrega una marca de agua de texto sin formato.
doc.Watermark.SetText("Aspose Watermark");

// Si deseamos editar el formato del texto usándolo como marca de agua,
// podemos hacerlo pasando un objeto TextWatermarkOptions al crear la marca de agua.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Podemos eliminar una marca de agua de un documento como este.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ver también

* class [Watermark](../)
* espacio de nombres [Aspose.Words](../../watermark/)
* asamblea [Aspose.Words](../../../)

---

## SetText(string, TextWatermarkOptions) {#settext_1}

Agrega una marca de agua de texto al documento.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| text | String | Texto que se muestra como una marca de agua. |
| options | TextWatermarkOptions | Define opciones adicionales para la marca de agua de texto. |

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza cuando la longitud del texto está fuera de rango o el texto contiene solo espacios en blanco. |
| ArgumentNullException | Se lanza cuando el texto es`nulo` . |

### Observaciones

La longitud del texto debe estar en el rango de 1 a 200 inclusive. El texto no puede`nulo` o contener solo espacios en blanco.

Si[`TextWatermarkOptions`](../../textwatermarkoptions/) es`nulo`, la marca de agua se configurará con las opciones predeterminadas.

### Ejemplos

Muestra cómo crear una marca de agua de texto.

```csharp
Document doc = new Document();

// Agrega una marca de agua de texto sin formato.
doc.Watermark.SetText("Aspose Watermark");

// Si deseamos editar el formato del texto usándolo como marca de agua,
// podemos hacerlo pasando un objeto TextWatermarkOptions al crear la marca de agua.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Podemos eliminar una marca de agua de un documento como este.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ver también

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* espacio de nombres [Aspose.Words](../../watermark/)
* asamblea [Aspose.Words](../../../)


