---
title: NodeImporter
second_title: Referencia de API de Aspose.Words para .NET
description: Permite realizar de manera eficiente la importación repetida de nodos de un documento a otro.
type: docs
weight: 3970
url: /es/net/aspose.words/nodeimporter/
---
## NodeImporter class

Permite realizar de manera eficiente la importación repetida de nodos de un documento a otro.

```csharp
public class NodeImporter
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [NodeImporter](nodeimporter#constructor)(DocumentBase, DocumentBase, ImportFormatMode) | Inicializa una nueva instancia del[`NodeImporter`](../nodeimporter) clase. |
| [NodeImporter](nodeimporter#constructor_1)(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) | Inicializa una nueva instancia del[`NodeImporter`](../nodeimporter) clase. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode)(Node, bool) | Importa un nodo de un documento a otro. |

### Observaciones

Aspose.Words proporciona funcionalidad para copiar y mover fácilmente fragments entre documentos de Microsoft Word. Esto se conoce como "importación de nodos". Antes de poder insertar un fragmento de un documento en otro, debe "importarlo". La importación crea un clon profundo del nodo original, listo para insertarse en el documento de destino .

La forma más sencilla de importar un nodo es utilizar el[`ImportNode`](../documentbase/importnode) method proporcionado por el[`DocumentBase`](../documentbase) objeto.

Sin embargo, cuando necesite importar nodos de un documento a otro varias veces, es mejor usar el[`NodeImporter`](../nodeimporter) clase. los[`NodeImporter`](../nodeimporter) La clase permite minimizar la cantidad de estilos y listas creadas en el documento de destino.

Copiar o mover fragmentos de un documento de Microsoft Word a otro presenta un número de desafíos técnicos para Aspose.Words. En un documento de Word, los estilos y el formato de lista se almacenan de forma centralizada, separados del texto del documento. Los párrafos y las tiradas de texto simplemente hacen referencia a los estilos mediante identificadores únicos internos.

Los desafíos surgen del hecho de que los estilos y las listas son diferentes en diferentes documentos. Por ejemplo, para copiar un párrafo formateado con el estilo Título 1 de un documento a otro, se deben tener en cuenta varias cosas: decidir si copie el estilo Título 1 de el documento de origen al documento de destino, clone el párrafo, actualice el párrafo clonado para que haga referencia al estilo Título 1 correcto en el documento de destino. Si el estilo tuvo que ser copiado, todos los estilos que las referencias (basadas en el estilo y el estilo del párrafo siguiente) deben analizarse y posiblemente copiarse también, etc.

los[`NodeImporter`](../nodeimporter)class es como un contexto, que contiene las "tablas de traducción" durante la importación. Traduce correctamente entre estilos y listas en los documentos de origen y de destino.

### Ejemplos

Muestra cómo insertar el contenido de un documento en un marcador de otro documento.

```csharp
[Test]
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

        // Recorre todos los nodos a nivel de bloque en el cuerpo de la sección,
        // luego clone e inserte cada nodo que no sea el último párrafo vacío de una sección.
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

* espacio de nombres [Aspose.Words](../../aspose.words)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
