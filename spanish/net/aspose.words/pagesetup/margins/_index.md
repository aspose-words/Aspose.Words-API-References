---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words para .NET
description: Ajuste fácilmente los márgenes de su página con la propiedad PageSetup. Personalice la configuración para un diseño y una presentación óptimos. ¡Mejore la apariencia de su documento!
type: docs
weight: 260
url: /es/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Devuelve o establece un valor preestablecido[`Margins`](../../margins/) de la página.

```csharp
public Margins Margins { get; set; }
```

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

* enum [Margins](../../margins/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
