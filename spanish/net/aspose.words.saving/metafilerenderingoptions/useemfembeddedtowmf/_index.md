---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad UseEmfEmbeddedToWmf optimiza la representación de metarchivos WMF, mejorando el rendimiento y la calidad de sus aplicaciones gráficas.
type: docs
weight: 70
url: /es/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Obtiene o establece un valor que determina cómo se deben representar los metarchivos WMF con metarchivos EMF integrados.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## Observaciones

Los metarchivos WMF pueden contener datos EMF incrustados. MS Word, en la mayoría de los casos, utiliza datos EMF incrustados. GDI+ siempre utiliza datos WMF.

Cuando este valor se establece en`verdadero`Aspose.Words utiliza datos EMF integrados durante la renderización.

Cuando este valor se establece en`FALSO`Aspose.Words utiliza datos WMF durante la renderización.

Esta opción solo se utiliza cuando el metarchivo se renderiza como gráfico vectorial. Cuando el metarchivo se renderiza como mapa de bits, siempre se utilizan datos WMF.

El valor predeterminado es`verdadero`.

## Ejemplos

Muestra cómo configurar las opciones de representación relacionadas con el metarchivo mejorado de Windows al guardar en PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establezca la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.Emf"
// para representar únicamente la parte EMF de un metarchivo dual EMF+.
// Establezca la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.EmfPlus" para
// para representar la parte EMF+ de un metarchivo dual EMF+.
// Establezca la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// para representar la parte EMF+ de un metarchivo dual EMF+ si se admiten todos los registros EMF+.
// De lo contrario, Aspose.Words representará la parte EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Establezca la propiedad "UseEmfEmbeddedToWmf" en "verdadero" para representar datos EMF incrustados
// para metarchivos que podemos representar como gráficos vectoriales.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Ver también

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
