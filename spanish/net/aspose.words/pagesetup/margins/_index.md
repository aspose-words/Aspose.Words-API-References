---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words para .NET
description: PageSetup Margins propiedad. Devuelve o establece valores preestablecidosMargins de la página en C#.
type: docs
weight: 260
url: /es/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Devuelve o establece valores preestablecidos[`Margins`](../../margins/) de la página.

```csharp
public Margins Margins { get; set; }
```

## Ejemplos

Muestra cuándo volver a calcular el diseño de página del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Guardar un documento en PDF, en una imagen o imprimirlo por primera vez se realizará automáticamente
// almacena en caché el diseño del documento dentro de sus páginas.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modificar el documento de alguna manera.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // En la versión actual de Aspose.Words, la modificación del documento no se reconstruye automáticamente
// el diseño de la página en caché. Si deseamos el diseño en caché
// para mantenernos actualizados, necesitaremos actualizarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Ver también

* enum [Margins](../../margins/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
