---
title: StructuredDocumentTag.Style
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTag propiedad. Obtiene o establece el Estilo de la etiqueta del documento estructurado.
type: docs
weight: 260
url: /es/net/aspose.words.markup/structureddocumenttag/style/
---
## StructuredDocumentTag.Style property

Obtiene o establece el Estilo de la etiqueta del documento estructurado.

```csharp
public Style Style { get; set; }
```

### Observaciones

SoloCharacter estilo oParagraph Se puede establecer un estilo con un estilo de carácter vinculado.

### Ejemplos

Muestra cómo trabajar con estilos para elementos de control de contenido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos formas de aplicar un estilo del documento a una etiqueta de documento estructurado.
// 1 - Aplicar un objeto de estilo de la colección de estilos del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Hacer referencia a un estilo en el documento por su nombre:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Ver también

* class [Style](../../../aspose.words/style/)
* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttag/)
* asamblea [Aspose.Words](../../../)


