---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Settings.MultiplePagesType para obtener opciones de impresión de documentos eficientes. ¡Optimice su flujo de trabajo con configuraciones de impresión flexibles!
type: docs
weight: 6700
url: /es/net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

Especifica cómo se imprime el documento.

```csharp
public enum MultiplePagesType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Normal | `0` | Impresión normal, sin especificar varias páginas. |
| MirrorMargins | `1` | Intercambia los márgenes izquierdo y derecho en páginas opuestas. |
| TwoPagesPerSheet | `2` | Imprime dos páginas por hoja. |
| BookFoldPrinting | `3` | Especifica si se debe imprimir el documento como un libro plegado. |
| BookFoldPrintingReverse | `4` | Especifica si se debe imprimir el documento como un libro plegado invertido. |
| Default | `0` | El valor predeterminado esNormal |

## Ejemplos

Muestra cómo configurar un documento que se puede imprimir como un libro plegable.

```csharp
Document doc = new Document();

// Insertar texto que abarca 16 páginas.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de libro plegable.
// Cuando imprimimos este documento por ambas caras, podemos tomar las páginas para apilarlas
// y dóblalos todos por la mitad a la vez. El contenido del documento se alineará formando un pliegue.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

//Solo podemos especificar el número de hojas en múltiplos de 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
