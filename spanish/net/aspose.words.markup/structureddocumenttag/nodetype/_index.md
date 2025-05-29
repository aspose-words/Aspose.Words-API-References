---
title: StructuredDocumentTag.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words para .NET
description: Explora la propiedad StructuredDocumentTag NodeType para una gestión documental eficiente. Accede sin problemas a los datos estructurados en tus proyectos.
type: docs
weight: 220
url: /es/net/aspose.words.markup/structureddocumenttag/nodetype/
---
## StructuredDocumentTag.NodeType property

DevuelveStructuredDocumentTag .

```csharp
public override NodeType NodeType { get; }
```

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
