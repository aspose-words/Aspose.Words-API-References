---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Markup.MarkupLevel, que define dónde encajan las StructuredDocumentTags en su árbol de documentos para una mejor organización y control.
type: docs
weight: 4670
url: /es/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Especifica el nivel en el árbol del documento donde se encuentra un documento en particular.[`StructuredDocumentTag`](../structureddocumenttag/) puede ocurrir.

```csharp
public enum MarkupLevel
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Unknown | `0` | Especifica el valor desconocido o no válido. |
| Inline | `1` | El elemento aparece en el nivel en línea (por ejemplo, entre líneas de texto). |
| Block | `2` | El elemento aparece a nivel de bloque (por ejemplo, entre tablas y párrafos). |
| Row | `3` | El elemento aparece entre filas de una tabla. |
| Cell | `4` | El elemento se encuentra entre celdas de una fila. |

## Ejemplos

Muestra cómo trabajar con estilos para elementos de control de contenido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

A continuación se muestran dos formas de aplicar un estilo del documento a una etiqueta de documento estructurado.
// 1 - Aplicar un objeto de estilo de la colección de estilos del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Hacer referencia a un estilo en el documento por nombre:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Ver también

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
