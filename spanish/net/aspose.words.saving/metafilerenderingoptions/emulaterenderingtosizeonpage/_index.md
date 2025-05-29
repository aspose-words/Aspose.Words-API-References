---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad EmulateRenderingToSizeOnPage mejora la representación de metarchivos, garantizando tamaños de visualización precisos para obtener resultados visuales óptimos.
type: docs
weight: 40
url: /es/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Obtiene o establece un valor que determina si la representación del metarchivo emula la visualización del metarchivo según el tamaño de la página o la visualización del metarchivo en su tamaño predeterminado.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Observaciones

Cuando se muestran metarchivos en MS Word, algunos gráficos pueden escalarse de acuerdo con el tamaño real del metarchivo en píxeles. Es decir, incluso el zoom puede afectar la visualización del metarchivo.

Cuando este valor se establece en`verdadero` Aspose.Words emula la representación según el tamaño del metarchivo en la página. El tamaño en píxeles se calcula a partir del tamaño del metarchivo en la página y el valor especificado.[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Cuando este valor se establece en`FALSO`Aspose.Words emula la representación de metarchivo a su tamaño predeterminado en píxeles.

Esta opción se utiliza sólo cuando el metarchivo se representa como gráficos vectoriales.

El valor predeterminado es`verdadero`.

## Ejemplos

Muestra cómo visualizar el metarchivo según el tamaño de la página.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establezca la propiedad "EmulateRenderingToSizeOnPage" en "verdadero"
// para emular la representación según el tamaño del metarchivo en la página.
// Establezca la propiedad "EmulateRenderingToSizeOnPage" en "falso"
// para emular la representación del metarchivo a su tamaño predeterminado en píxeles.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Ver también

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
