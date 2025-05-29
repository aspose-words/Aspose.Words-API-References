---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words para .NET
description: Modernice la estructura de su documento con el método UpdatePageLayout, garantizando un diseño pulido y organizado para una mejor legibilidad y presentación.
type: docs
weight: 830
url: /es/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Reconstruye el diseño de página del documento.

```csharp
public void UpdatePageLayout()
```

## Observaciones

Este método formatea un documento en páginas y actualiza los campos relacionados con el número de página, como PÁGINA, PÁGINAS, REF.PAG. y REF. La información actualizada del diseño de página es necesaria para una correcta representación del documento en formatos de página fijos.

Este método se invoca automáticamente al convertir un documento a PDF, XPS o imagen por primera vez, o al imprimirlo. Sin embargo, si modifica el documento después de renderizarlo y luego intenta renderizarlo de nuevo, Aspose.Words no actualizará el diseño de página automáticamente. En ese caso, debe llamar a`UpdatePageLayout` before renderizando nuevamente.

## Ejemplos

Muestra cuándo recalcular el diseño de página del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Guardar un documento como PDF, como imagen o imprimirlo por primera vez se realizará automáticamente
// almacena en caché el diseño del documento dentro de sus páginas.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

//Modificar el documento de alguna manera.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// En la versión actual de Aspose.Words, modificar el documento no lo reconstruye automáticamente
// El diseño de la página en caché. Si deseamos el diseño en caché
// Para mantenernos actualizados, necesitaremos actualizarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
