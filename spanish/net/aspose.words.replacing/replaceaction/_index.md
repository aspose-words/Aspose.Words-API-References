---
title: ReplaceAction Enum
linktitle: ReplaceAction
articleTitle: ReplaceAction
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.ReplaceAction para controlar los resultados de las coincidencias en sus operaciones de reemplazo, mejorando la eficiencia y la precisión de la edición de documentos.
type: docs
weight: 5370
url: /es/net/aspose.words.replacing/replaceaction/
---
## ReplaceAction enumeration

Permite al usuario especificar qué sucede con la coincidencia actual durante una operación de reemplazo.

```csharp
public enum ReplaceAction
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Replace | `0` | Reemplazar la coincidencia actual. |
| Skip | `1` | Omitir la coincidencia actual. |
| Stop | `2` | Terminar la operación de reemplazo. |

## Ejemplos

Muestra cómo insertar el contenido de un documento completo como reemplazo de una coincidencia en una operación de búsqueda y reemplazo.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Insertar un documento después del párrafo que contiene el texto coincidente.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        //Elimina el párrafo con el texto coincidente.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Inserta todos los nodos de otro documento después de un párrafo o tabla.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Omite el nodo si es el último párrafo vacío de una sección.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### Ver también

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* espacio de nombres [Aspose.Words.Replacing](../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../)
