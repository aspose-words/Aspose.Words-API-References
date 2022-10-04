---
title: ReplacingArgs
second_title: Referencia de API de Aspose.Words para .NET
description: Proporciona datos para una operación de reemplazo personalizada.
type: docs
weight: 4390
url: /es/net/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class

Proporciona datos para una operación de reemplazo personalizada.

```csharp
public class ReplacingArgs
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [GroupIndex](../../aspose.words.replacing/replacingargs/groupindex/) { get; set; } | Identifica, por índice, un grupo capturado en el[`Match`](./match/) que se va a reemplazar con el[`Replacement`](./replacement/) cadena. |
| [GroupName](../../aspose.words.replacing/replacingargs/groupname/) { get; set; } | Identifica, por su nombre, un grupo capturado en el[`Match`](./match/) que se va a reemplazar con el[`Replacement`](./replacement/) cadena. |
| [Match](../../aspose.words.replacing/replacingargs/match/) { get; } | ElMatch resultado de una única coincidencia de expresión regular durante una **Reemplazar** . |
| [MatchNode](../../aspose.words.replacing/replacingargs/matchnode/) { get; } | Obtiene el nodo que contiene el comienzo de la coincidencia. |
| [MatchOffset](../../aspose.words.replacing/replacingargs/matchoffset/) { get; } | Obtiene la posición inicial basada en cero de la coincidencia desde el inicio de el nodo que contiene el comienzo de la coincidencia. |
| [Replacement](../../aspose.words.replacing/replacingargs/replacement/) { get; set; } | Obtiene o establece la cadena de reemplazo. |

### Ejemplos

Muestra cómo reemplazar todas las apariciones de un patrón de expresión regular con otra cadena, mientras realiza un seguimiento de todos esos reemplazos.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
    FindReplaceOptions options = new FindReplaceOptions();

    // Establezca una devolución de llamada que realice un seguimiento de los reemplazos que realizará el método "Reemplazar".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Mantiene un registro de cada reemplazo de texto realizado por una operación de buscar y reemplazar
/// y anota el valor del texto coincidente original.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

Muestra cómo insertar el contenido de un documento completo como reemplazo de una coincidencia en una operación de buscar y reemplazar.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Inserta un documento después del párrafo que contiene el texto coincidente.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Eliminar el párrafo con el texto coincidente.
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
                // Omite el nodo si es el último párrafo vacío en una sección.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
