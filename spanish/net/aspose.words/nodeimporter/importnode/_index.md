---
title: NodeImporter.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words para .NET
description: Transfiera nodos entre documentos fácilmente con el método ImportNode de NodeImporter. ¡Mejore su flujo de trabajo y agilice la integración de datos hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

Importa un nodo de un documento a otro.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcNode | Node | El nodo a importar. |
| isImportChildren | Boolean | `verdadero` para importar todos los nodos secundarios de forma recursiva; de lo contrario,`FALSO`. |

### Valor_devuelto

El nodo clonado e importado. Pertenece al documento de destino, pero no tiene padre.

## Observaciones

Al importar un nodo, se crea una copia del nodo de origen perteneciente al documento importador. El nodo devuelto no tiene padre. El nodo de origen no se modifica ni se elimina del documento original.

Antes de insertar un nodo de otro documento en este, debe importarse. Durante la importación, las propiedades específicas del documento, como las referencias a estilos y listas, se traducen del original al documento de importación. Una vez importado el nodo, se puede insertar en el lugar correspondiente del documento mediante[`InsertBefore`](../../compositenode/insertbefore/) o [`InsertAfter`](../../compositenode/insertafter/).

Si el nodo de origen ya pertenece al documento de destino, entonces simplemente se crea un clone profundo del nodo de origen.

## Ejemplos

Muestra cómo insertar el contenido de un documento en un marcador de otro documento.

```csharp
public void InsertAtBookmark()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("InsertionPoint");
    builder.Write("We will insert a document here: ");
    builder.EndBookmark("InsertionPoint");

    Document docToInsert = new Document();
    builder = new DocumentBuilder(docToInsert);

    builder.Write("Hello world!");

    docToInsert.Save(ArtifactsDir + "NodeImporter.InsertAtMergeField.docx");

    Bookmark bookmark = doc.Range.Bookmarks["InsertionPoint"];
    InsertDocument(bookmark.BookmarkStart.ParentNode, docToInsert);

    Assert.AreEqual("We will insert a document here: " +
                    "\rHello world!", doc.GetText().Trim());
}

/// <summary>
/// Inserta el contenido de un documento después del nodo especificado.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Recorre todos los nodos de nivel de bloque en el cuerpo de la sección,
        // luego clona e inserta cada nodo que no sea el último párrafo vacío de una sección.
        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                destinationParent.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node should be either a paragraph or table.");
    }
}
```

### Ver también

* class [Node](../../node/)
* class [NodeImporter](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
