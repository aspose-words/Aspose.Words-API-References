---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words para .NET
description: Descubre la enumeración Aspose.Words.Margins para personalizar los márgenes de tus documentos. ¡Mejora el formato de tus documentos con ajustes preestablecidos fáciles de usar!
type: docs
weight: 4580
url: /es/net/aspose.words/margins/
---
## Margins enumeration

Especifica márgenes preestablecidos.

```csharp
public enum Margins
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Normal | `0` | Márgenes normales. |
| Narrow | `1` | Márgenes estrechos. |
| Moderate | `2` | Márgenes moderados. |
| Wide | `3` | Márgenes amplios. |
| Mirrored | `4` | Márgenes reflejados. |
| Custom | `5` | Márgenes personalizados. |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
