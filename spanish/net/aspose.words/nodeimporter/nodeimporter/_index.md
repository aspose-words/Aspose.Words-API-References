---
title: NodeImporter
second_title: Referencia de API de Aspose.Words para .NET
description: Inicializa una nueva instancia delNodeImporteraspose.words/nodeimporter clase.
type: docs
weight: 10
url: /es/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode) {#constructor}

Inicializa una nueva instancia del[`NodeImporter`](../../nodeimporter) clase.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcDoc | DocumentBase | El documento fuente. |
| dstDoc | DocumentBase | El documento de destino que será el propietario de los nodos importados. |
| importFormatMode | ImportFormatMode | Especifica cómo fusionar el formato de estilo que entra en conflicto. |

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

* class [DocumentBase](../../documentbase)
* enum [ImportFormatMode](../../importformatmode)
* class [NodeImporter](../../nodeimporter)
* espacio de nombres [Aspose.Words](../../nodeimporter)
* asamblea [Aspose.Words](../../../)

---

## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) {#constructor_1}

Inicializa una nueva instancia del[`NodeImporter`](../../nodeimporter) clase.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcDoc | DocumentBase | El documento fuente. |
| dstDoc | DocumentBase | El documento de destino que será el propietario de los nodos importados. |
| importFormatMode | ImportFormatMode | Especifica cómo fusionar el formato de estilo que entra en conflicto. |
| importFormatOptions | ImportFormatOptions | Especifica varias opciones para dar formato al nodo importado. |

### Ejemplos

Muestra cómo resolver un conflicto al importar documentos que tienen listas con el mismo identificador de definición de lista.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Establecer la propiedad "KeepSourceNumbering" en "true" para aplicar un ID de definición de lista diferente
// a estilos idénticos a los de Aspose.Words los importa a los documentos de destino.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Muestra cómo resolver conflictos de numeración de listas en documentos de origen y destino.

```csharp
// Abra un documento con un esquema de numeración de lista personalizado y luego clónelo.
// Dado que ambos tienen el mismo formato de numeración, los formatos chocarán si importamos un documento en el otro.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Cuando importamos el clon del documento al original y luego lo agregamos,
// luego se unirán las dos listas con el mismo formato de lista.
// Si establecemos el indicador "KeepSourceNumbering" en "falso", entonces la lista del documento se clona
// que agregamos al original continuará con la numeración de la lista a la que lo agregamos.
// Esto fusionará efectivamente las dos listas en una sola.
// Si establecemos el indicador "KeepSourceNumbering" en "true", entonces el documento se clona
// la lista conservará su numeración original, haciendo que las dos listas aparezcan como listas separadas. 
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Ver también

* class [DocumentBase](../../documentbase)
* enum [ImportFormatMode](../../importformatmode)
* class [ImportFormatOptions](../../importformatoptions)
* class [NodeImporter](../../nodeimporter)
* espacio de nombres [Aspose.Words](../../nodeimporter)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
