---
title: IReplacingCallback.Replacing
second_title: Referencia de API de Aspose.Words para .NET
description: IReplacingCallback método. Un método definido por el usuario que se llama durante una operación de reemplazo para cada coincidencia encontrada justo antes de realizar un reemplazo.
type: docs
weight: 10
url: /es/net/aspose.words.replacing/ireplacingcallback/replacing/
---
## IReplacingCallback.Replacing method

Un método definido por el usuario que se llama durante una operación de reemplazo para cada coincidencia encontrada justo antes de realizar un reemplazo.

```csharp
public ReplaceAction Replacing(ReplacingArgs args)
```

### Valor_devuelto

A[`ReplaceAction`](../../replaceaction/) valor que especifica la acción a realizar para la coincidencia actual.

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

* enum [ReplaceAction](../../replaceaction/)
* class [ReplacingArgs](../../replacingargs/)
* interface [IReplacingCallback](../)
* espacio de nombres [Aspose.Words.Replacing](../../ireplacingcallback/)
* asamblea [Aspose.Words](../../../)


