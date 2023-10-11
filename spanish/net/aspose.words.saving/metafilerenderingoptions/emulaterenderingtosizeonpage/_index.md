---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
second_title: Referencia de API de Aspose.Words para .NET
description: MetafileRenderingOptions propiedad. Obtiene o establece un valor que determina si la representación del metarchivo emula la visualización del metarchivo según el tamaño en la página o la visualización del metarchivo en su tamaño predeterminado.
type: docs
weight: 40
url: /es/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Obtiene o establece un valor que determina si la representación del metarchivo emula la visualización del metarchivo según el tamaño en la página o la visualización del metarchivo en su tamaño predeterminado.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

### Observaciones

Cuando los metarchivos se muestran en MS Word, algunos gráficos pueden escalarse de acuerdo con el tamaño real del metarchivo en píxeles. Es decir, incluso el zoom puede afectar la visualización del metarchivo.

Cuando este valor se establece en`verdadero` Aspose.Words emula la representación según el tamaño del metarchivo en la página. El tamaño en píxeles se calcula a partir del tamaño del metarchivo en la página y el especificado[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Cuando este valor se establece en`FALSO`, Aspose.Words emula la representación de metarchivos a su tamaño predeterminado en píxeles.

Esta opción se utiliza sólo cuando el metarchivo se representa como gráficos vectoriales.

El valor predeterminado es`verdadero`.

### Ejemplos

Muestra cómo visualizar el metarchivo según el tamaño de la página.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establece la propiedad "EmulateRenderingToSizeOnPage" en "true"
// para emular la representación según el tamaño del metarchivo en la página.
// Establece la propiedad "EmulateRenderingToSizeOnPage" en "falso"
// para emular la representación del metarchivo a su tamaño predeterminado en píxeles.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Ver también

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../metafilerenderingoptions/)
* asamblea [Aspose.Words](../../../)


