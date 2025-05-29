---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words para .NET
description: Descubra el método GetChildNodes de IStructuredDocumentTag y acceda a una colección dinámica de nodos secundarios adaptados a sus tipos específicos para una mejor gestión de documentos.
type: docs
weight: 170
url: /es/net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

Devuelve una colección activa de nodos secundarios que coinciden con los tipos especificados.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

## Ejemplos

Muestra cómo eliminar la etiqueta de documento estructurado, pero mantiene el contenido dentro.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Esta colección proporciona una interfaz unificada para acceder a etiquetas estructuradas con y sin rango.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Aquí podemos obtener nodos secundarios de la interfaz común de etiquetas estructuradas con rango y sin rango.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Ver también

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
