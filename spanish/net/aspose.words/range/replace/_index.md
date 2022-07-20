---
title: Replace
second_title: Referencia de API de Aspose.Words para .NET
description: Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo.
type: docs
weight: 80
url: /es/net/aspose.words/range/replace/
---
## Replace(string, string) {#replace}

Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo.

```csharp
public int Replace(string pattern, string replacement)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pattern | String | Una cadena para ser reemplazada. |
| replacement | String | Una cadena para reemplazar todas las apariciones de patrón. |

### Valor_devuelto

El número de reemplazos realizados.

### Observaciones

El patrón no se utilizará como expresión regular. Utilice[`Replace`](../replace) si necesita expresiones regulares.

Comparación que no distingue entre mayúsculas y minúsculas.

El método puede procesar rupturas tanto en el patrón como en las cadenas de reemplazo.

Debe usar metacaracteres especiales si necesita trabajar con pausas:

* **&amp;pags** - salto de párrafo
* **&amp;b** - salto de sección
* **&amp;metro** - salto de página
* **&amp;l** - salto de línea manual

Usar método[`Replace`](../replace) para tener una personalización más flexible.

### Ejemplos

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Inserta un salto de párrafo después de Números.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Muestra cómo realizar una operación de buscar y reemplazar texto en el contenido de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Realizar una operación de búsqueda y reemplazo en el contenido de nuestro documento y verificar la cantidad de reemplazos que se realizaron.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

Muestra cómo agregar formato a los párrafos en los que una operación de buscar y reemplazar ha encontrado coincidencias.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establecer la propiedad "Alineación" en "ParagraphAlignment.Right" para alinear a la derecha cada párrafo
// que contiene una coincidencia que encuentra la operación de buscar y reemplazar.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Reemplace cada punto que está justo antes de un salto de párrafo con un signo de exclamación.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Ver también

* class [Range](../../range)
* espacio de nombres [Aspose.Words](../../range)
* asamblea [Aspose.Words](../../../)

---

## Replace(Regex, string) {#replace_2}

Reemplaza todas las apariciones de un patrón de caracteres especificado por una expresión regular con otra cadena.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pattern | Regex | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| replacement | String | Una cadena para reemplazar todas las apariciones de patrón. |

### Valor_devuelto

El número de reemplazos realizados.

### Observaciones

Reemplaza toda la coincidencia capturada por la expresión regular.

El método puede procesar rupturas tanto en el patrón como en las cadenas de reemplazo.

Debe usar metacaracteres especiales si necesita trabajar con pausas:

* **&amp;pags** - salto de párrafo
* **&amp;b** - salto de sección
* **&amp;metro** - salto de página
* **&amp;l** - salto de línea manual

Usar método[`Replace`](../replace) para tener una personalización más flexible.

### Ejemplos

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Reemplaza cada número con un salto de párrafo.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Muestra cómo reemplazar todas las apariciones de un patrón de expresión regular con otro texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### Ver también

* class [Range](../../range)
* espacio de nombres [Aspose.Words](../../range)
* asamblea [Aspose.Words](../../../)

---

## Replace(string, string, FindReplaceOptions) {#replace_1}

Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pattern | String | Una cadena para ser reemplazada. |
| replacement | String | Una cadena para reemplazar todas las apariciones de patrón. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions) objeto para especificar opciones adicionales. |

### Valor_devuelto

El número de reemplazos realizados.

### Observaciones

El patrón no se utilizará como expresión regular. Utilice[`Replace`](../replace) si necesita expresiones regulares.

El método puede procesar rupturas tanto en el patrón como en las cadenas de reemplazo.

Debe usar metacaracteres especiales si necesita trabajar con pausas:

* **&amp;pags** - salto de párrafo
* **&amp;b** - salto de sección
* **&amp;metro** - salto de página
* **&amp;l** - salto de línea manual
* **&amp;&amp;** - &amp; personaje

### Ejemplos

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Inserta un salto de párrafo después de Números.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Muestra cómo reemplazar texto en el pie de página de un documento.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Muestra cómo alternar entre mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "MatchCase" en "verdadero" para aplicar la distinción entre mayúsculas y minúsculas mientras busca cadenas para reemplazar.
// Establezca el indicador "MatchCase" en "falso" para ignorar las mayúsculas y minúsculas mientras busca texto para reemplazar.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Muestra cómo alternar operaciones independientes de búsqueda y reemplazo de solo palabras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "FindWholeWordsOnly" en "true" para reemplazar el texto encontrado si no forma parte de otra palabra.
// Establezca el indicador "FindWholeWordsOnly" en "falso" para reemplazar todo el texto independientemente de su entorno.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Muestra cómo reemplazar todas las instancias de Cadena de texto en una tabla y celda.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

// Realizar una operación de buscar y reemplazar en una tabla completa.
table.Range.Replace("Carrots", "Eggs", options);

// Realiza una operación de buscar y reemplazar en la última celda de la última fila de la tabla.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* espacio de nombres [Aspose.Words](../../range)
* asamblea [Aspose.Words](../../../)

---

## Replace(Regex, string, FindReplaceOptions) {#replace_3}

Reemplaza todas las apariciones de un patrón de caracteres especificado por una expresión regular con otra cadena.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pattern | Regex | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| replacement | String | Una cadena para reemplazar todas las apariciones de patrón. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions) objeto para especificar opciones adicionales. |

### Valor_devuelto

El número de reemplazos realizados.

### Observaciones

Reemplaza toda la coincidencia capturada por la expresión regular.

El método puede procesar rupturas tanto en el patrón como en las cadenas de reemplazo.

Debe usar metacaracteres especiales si necesita trabajar con pausas:

* **&amp;pags** - salto de párrafo
* **&amp;b** - salto de sección
* **&amp;metro** - salto de página
* **&amp;l** - salto de línea manual
* **&amp;&amp;** - &amp; personaje

### Ejemplos

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Reemplaza cada número con un salto de párrafo.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

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

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* espacio de nombres [Aspose.Words](../../range)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
