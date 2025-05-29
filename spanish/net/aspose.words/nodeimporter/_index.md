---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words para .NET
description: Transfiera nodos de documentos fácilmente con Aspose.Words.NodeImporter. ¡Optimice su flujo de trabajo y mejore la eficiencia de la gestión documental hoy mismo!
type: docs
weight: 4900
url: /es/net/aspose.words/nodeimporter/
---
## NodeImporter class

Permite realizar de manera eficiente la importación repetida de nodos de un documento a otro.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Artículo de documentación.

```csharp
public class NodeImporter
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Inicializa una nueva instancia del`NodeImporter` clase. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Inicializa una nueva instancia del`NodeImporter` clase. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Importa un nodo de un documento a otro. |

## Observaciones

Aspose.Words ofrece una función para copiar y mover fragmentos fácilmente entre documentos de Microsoft Word. Esto se conoce como "importar nodos". Antes de insertar un fragmento de un documento en otro, es necesario "importarlo". La importación crea un clon profundo del nodo original, listo para insertarse en el documento de destino.

La forma más sencilla de importar un nodo es utilizar el[`ImportNode`](../documentbase/importnode/) método proporcionado por el[`DocumentBase`](../documentbase/) objeto.

Sin embargo, cuando necesita importar nodos de un documento a otro varias veces, es mejor utilizar el`NodeImporter` clase. La`NodeImporter` La clase permite minimizar la cantidad de estilos y listas creadas en el documento de destino.

Copiar o mover fragmentos de un documento de Microsoft Word a otro presenta numerosos desafíos técnicos para Aspose.Words. En un documento de Word, los estilos y el formato de lista se almacenan de forma centralizada, separados del texto. Los párrafos y las secuencias de texto simplemente hacen referencia a los estilos mediante identificadores únicos internos.

Los desafíos surgen del hecho de que los estilos y las listas son diferentes en distintos documentos. Por ejemplo, para copiar un párrafo formateado con el estilo Encabezado 1 de un documento a otro, se deben tener en cuenta varias cosas: decidir si se copia el estilo Encabezado 1 del documento de origen al documento de destino, clonar el párrafo, actualizar el párrafo clonado para que haga referencia al estilo Encabezado 1 correcto en el documento de destino. Si se tuviera que copiar el estilo, se deberían analizar y posiblemente copiar también todos los estilos a los que hace referencia (según el estilo y el estilo del párrafo siguiente), y así sucesivamente. Existen problemas similares al copiar párrafos numerados o con viñetas porque Microsoft Word almacena las definiciones de lista por separado del texto.

El`NodeImporter`La clase es como un contexto que contiene las tablas de traducción durante la importación. Realiza la traducción correcta entre estilos y listas en los documentos de origen y destino.

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
