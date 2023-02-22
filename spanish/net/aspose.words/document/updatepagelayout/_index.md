---
title: Document.UpdatePageLayout
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Reconstruye el diseño de página del documento.
type: docs
weight: 750
url: /es/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Reconstruye el diseño de página del documento.

```csharp
public void UpdatePageLayout()
```

### Observaciones

Este método formatea un documento en páginas y actualiza los campos relacionados con el número de página en el documento, como como PÁGINA, PÁGINAS, PAGEREF y REF. La información de diseño de página actualizada es necesaria para una representación correcta del documento en formatos de página fijos.

Este método se invoca automáticamente cuando convierte por primera vez un documento a PDF, XPS, imagen o lo imprime. Sin embargo, si modifica el documento después de renderizarlo y luego intenta renderizarlo de nuevo, Aspose.Words no actualizará el diseño de la página automáticamente. En este caso debe llamar`UpdatePageLayout` before renderizado de nuevo.

### Ejemplos

Muestra cuándo recalcular el diseño de página del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Guardar un documento en PDF, en una imagen o imprimirlo por primera vez automáticamente
// almacena en caché el diseño del documento dentro de sus páginas.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modificar el documento de alguna manera.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;

  // En la versión actual de Aspose.Words, la modificación del documento no se reconstruye automáticamente
// el diseño de la página en caché. Si deseamos el diseño en caché
// para estar actualizado, necesitaremos actualizarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


