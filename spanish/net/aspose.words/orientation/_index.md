---
title: Orientation Enum
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Orientation para un control preciso de la orientación de las páginas. ¡Mejore el formato de sus documentos con facilidad y precisión!
type: docs
weight: 5050
url: /es/net/aspose.words/orientation/
---
## Orientation enumeration

Especifica la orientación de la página.

```csharp
public enum Orientation
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Portrait | `1` | Orientación de página vertical (estrecha y alta). |
| Landscape | `2` | Orientación de página horizontal (ancha y corta). |

## Ejemplos

Muestra cómo aplicar y revertir configuraciones de configuración de página a secciones de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifique las propiedades de configuración de la página para la sección actual del constructor y agregue texto.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si comenzamos una nueva sección usando un generador de documentos,
// heredará las propiedades de configuración de página actual del constructor.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

//Podemos revertir sus propiedades de configuración de página a sus valores predeterminados usando el método "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
