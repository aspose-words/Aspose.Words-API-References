---
title: Range.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words para .NET
description: Reemplace fácilmente todas las instancias de un patrón de cadena de caracteres con el método "Reemplazo de rango". ¡Mejore su procesamiento de texto con esta potente herramienta!
type: docs
weight: 100
url: /es/net/aspose.words/range/replace/
---
## Replace(*string, string*) {#replace}

Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo.

```csharp
public int Replace(string pattern, string replacement)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pattern | String | Una cadena que debe reemplazarse. |
| replacement | String | Una cadena para reemplazar todas las apariciones del patrón. |

### Valor_devuelto

El número de reemplazos realizados.

## Observaciones

El patrón no se utilizará como expresión regular. Por favor, utilice`Replace` Si necesita expresiones regulares.

Se utilizó una comparación sin distinción entre mayúsculas y minúsculas.

El método puede procesar rupturas tanto en cadenas de patrones como de reemplazo.

Debes utilizar metacaracteres especiales si necesitas trabajar con saltos:

* **&amp;pag** - salto de párrafo
* **&amp;b** - salto de sección
* **&amp;metro** - salto de página
* **&amp;l** - salto de línea manual

Utilizar método`Replace` para tener una personalización más flexible.

## Ejemplos

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Inserta un salto de párrafo después de Números.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Muestra cómo realizar una operación de búsqueda y reemplazo de texto en el contenido de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Realice una operación de búsqueda y reemplazo en el contenido de nuestro documento y verifique la cantidad de reemplazos que se realizaron.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

Muestra cómo agregar formato a los párrafos en los que una operación de búsqueda y reemplazo encontró coincidencias.

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

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca la propiedad "Alineación" en "ParagraphAlignment.Right" para alinear a la derecha cada párrafo
// que contiene una coincidencia que la operación de buscar y reemplazar encuentra.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Reemplace cada punto que esté justo antes de un salto de párrafo con un signo de exclamación.
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

* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Replace(*Regex, string*) {#replace_2}

Reemplaza todas las ocurrencias de un patrón de caracteres especificado por una expresión regular con otra cadena.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pattern | Regex | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| replacement | String | Una cadena para reemplazar todas las apariciones del patrón. |

### Valor_devuelto

El número de reemplazos realizados.

## Observaciones

Reemplaza toda la coincidencia capturada por la expresión regular.

El método puede procesar rupturas tanto en cadenas de patrones como de reemplazo.

Debes utilizar metacaracteres especiales si necesitas trabajar con saltos:

* **&amp;pag** - salto de párrafo
* **&amp;b** - salto de sección
* **&amp;metro** - salto de página
* **&amp;l** - salto de línea manual

Utilizar método`Replace` para tener una personalización más flexible.

## Ejemplos

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Reemplaza cada número con un salto de párrafo.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Muestra cómo reemplazar todas las ocurrencias de un patrón de expresión regular con otro texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### Ver también

* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Replace(*string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pattern | String | Una cadena que debe reemplazarse. |
| replacement | String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### Valor_devuelto

El número de reemplazos realizados.

## Observaciones

El patrón no se utilizará como expresión regular. Por favor, utilice`Replace` Si necesita expresiones regulares.

El método puede procesar rupturas tanto en cadenas de patrones como de reemplazo.

Debes utilizar metacaracteres especiales si necesitas trabajar con saltos:

* **&amp;pag** - salto de párrafo
* **&amp;b** - salto de sección
* **&amp;metro** - salto de página
* **&amp;l** - salto de línea manual
* **&amp;&amp;** - &amp; personaje

## Ejemplos

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

Muestra cómo alternar la distinción entre mayúsculas y minúsculas al realizar una operación de búsqueda y reemplazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "MatchCase" en "verdadero" para aplicar distinción entre mayúsculas y minúsculas al buscar cadenas para reemplazar.
// Establezca el indicador "MatchCase" en "falso" para ignorar las mayúsculas y minúsculas mientras busca texto para reemplazar.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Muestra cómo alternar operaciones de búsqueda y reemplazo independientes de solo palabras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "FindWholeWordsOnly" en "verdadero" para reemplazar el texto encontrado si no es parte de otra palabra.
// Establezca el indicador "FindWholeWordsOnly" en "falso" para reemplazar todo el texto independientemente de su entorno.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Muestra cómo reemplazar todas las instancias de una cadena de texto en una tabla y celda.

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

// Realizar una operación de búsqueda y reemplazo en una tabla completa.
table.Range.Replace("Carrots", "Eggs", options);

//Realiza una operación de búsqueda y reemplazo en la última celda de la última fila de la tabla.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Replace(*Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

Reemplaza todas las ocurrencias de un patrón de caracteres especificado por una expresión regular con otra cadena.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pattern | Regex | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| replacement | String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### Valor_devuelto

El número de reemplazos realizados.

## Observaciones

Reemplaza toda la coincidencia capturada por la expresión regular.

El método puede procesar rupturas tanto en cadenas de patrones como de reemplazo.

Debes utilizar metacaracteres especiales si necesitas trabajar con saltos:

* **&amp;pag** - salto de párrafo
* **&amp;b** - salto de sección
* **&amp;metro** - salto de página
* **&amp;l** - salto de línea manual
* **&amp;&amp;** - &amp; personaje

## Ejemplos

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Reemplaza cada número con un salto de párrafo.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

Muestra cómo reemplazar todas las ocurrencias de un patrón de expresión regular con otra cadena, mientras se rastrean todos dichos reemplazos.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
    FindReplaceOptions options = new FindReplaceOptions();

    // Establezca una devolución de llamada que rastree cualquier reemplazo que realizará el método "Reemplazar".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Mantiene un registro de cada reemplazo de texto realizado mediante una operación de búsqueda y reemplazo
/// y anota el valor del texto original coincidente.
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

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
