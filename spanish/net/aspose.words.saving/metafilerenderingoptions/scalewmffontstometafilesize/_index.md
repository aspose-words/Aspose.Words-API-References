---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
second_title: Referencia de API de Aspose.Words para .NET
description: MetafileRenderingOptions propiedad. Obtiene o establece un valor que determina si escalar o no las fuentes en el metarchivo WMF según el tamaño del metarchivo en la página.
type: docs
weight: 50
url: /es/net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

Obtiene o establece un valor que determina si escalar o no las fuentes en el metarchivo WMF según el tamaño del metarchivo en la página.

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

### Observaciones

Cuando los metarchivos WMF se muestran en MS Word, las fuentes se pueden escalar según el tamaño real del metarchivo en la página.

Cuando este valor se establece en`verdadero`, Aspose.Words emula la escala de fuentes según el tamaño del metarchivo en la página.

Cuando este valor se establece en`falso`, Aspose.Words muestra las fuentes a medida que el metarchivo se representa en su tamaño predeterminado.

Esta opción se usa solo cuando el metarchivo se representa como gráficos vectoriales.

El valor predeterminado es`verdadero`.

### Ejemplos

Muestra cómo escalar las fuentes WMF según el tamaño del metarchivo en la página.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establecer la propiedad "ScaleWmfFontsToMetafileSize" en "true" para escalar las fuentes
// que dan formato al texto dentro de las imágenes WMF según el tamaño del metarchivo en la página.
// Establecer la propiedad "ScaleWmfFontsToMetafileSize" en "falso" para
// preservar la escala predeterminada de estas fuentes.
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### Ver también

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../metafilerenderingoptions/)
* asamblea [Aspose.Words](../../../)


