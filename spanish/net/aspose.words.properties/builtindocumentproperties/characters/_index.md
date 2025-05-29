---
title: BuiltInDocumentProperties.Characters
linktitle: Characters
articleTitle: Characters
second_title: Aspose.Words para .NET
description: Descubra la propiedad Caracteres BuiltInDocumentProperties, que proporciona una estimación precisa del recuento de caracteres para mejorar la gestión y la eficiencia de los documentos.
type: docs
weight: 40
url: /es/net/aspose.words.properties/builtindocumentproperties/characters/
---
## BuiltInDocumentProperties.Characters property

Representa una estimación del número de caracteres del documento.

```csharp
public int Characters { get; set; }
```

## Observaciones

Aspose.Words actualiza esta propiedad cuando llamas[`UpdateWordCount`](../../../aspose.words/document/updatewordcount/).

## Ejemplos

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words no realiza un seguimiento de métricas de documentos como estas en tiempo real.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Para obtener valores precisos para tres de estas propiedades, necesitaremos actualizarlas manualmente.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Para el conteo de líneas, necesitaremos llamar a una sobrecarga específica del método de actualización.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

Muestra cómo trabajar con las propiedades del documento en la categoría "Contenido".

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Mediante el uso de propiedades integradas,
    // Podemos tratar las estadísticas del documento, como el recuento de palabras, páginas y caracteres, como metadatos que se pueden consultar rápidamente sin abrir el documento.
    // Se accede a estas propiedades haciendo clic derecho en el archivo en el Explorador de Windows y navegando a Propiedades > Detalles > Contenido
    // Si queremos mostrar estos datos dentro del documento, podemos utilizar campos como NUMPAGES, NUMWORDS, NUMCHARS etc.
    // Además, estos valores también se pueden ver en Microsoft Word navegando a Archivo > Propiedades > Propiedades avanzadas > Estadísticas
    // Conteo de páginas: La propiedad PageCount muestra el conteo de páginas en tiempo real y su valor se puede asignar a la propiedad Pages

     //La propiedad "Páginas" almacena el número de páginas del documento.
    Assert.AreEqual(6, properties.Pages);

    // Las propiedades integradas "Palabras", "Caracteres" y "CaracteresConEspacios" también muestran varias estadísticas del documento,
    // pero necesitamos llamar al método "UpdateWordCount" en todo el documento antes de poder esperar que contengan valores precisos.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Cuente el número de líneas en el documento y luego asigne el resultado a la propiedad incorporada "Líneas".
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Asigna el número de nodos de párrafo en el documento a la propiedad incorporada "Párrafos".
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Obtenga una estimación del tamaño del archivo de nuestro documento a través de la propiedad incorporada "Bytes".
    Assert.AreEqual(20310, properties.Bytes);

    // Establezca una plantilla diferente para nuestro documento y luego actualice la propiedad incorporada "Plantilla" manualmente para reflejar este cambio.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" es una propiedad descriptiva incorporada.
    properties.ContentStatus = "Draft";

    // Al guardar, la propiedad incorporada "ContentType" contendrá el tipo MIME del formato de guardado de salida.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Si el documento contiene enlaces y todos están actualizados, podemos establecer la propiedad "LinksUpToDate" en "true".
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Cuenta las líneas de un documento.
/// Recorre el árbol de entidades de diseño del documento durante la construcción.
/// contando entidades del tipo "Línea" que también contienen texto real.
/// </summary>
private class LineCounter
{
    public LineCounter(Document doc)
    {
        mLayoutEnumerator = new LayoutEnumerator(doc);

        CountLines();
    }

    public int GetLineCount()
    {
        return mLineCount;
    }

    private void CountLines()
    {
        do
        {
            if (mLayoutEnumerator.Type == LayoutEntityType.Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator.MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator.Kind.StartsWith("TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator.MoveParent();
            }
        } while (mLayoutEnumerator.MoveNext());
    }

    private readonly LayoutEnumerator mLayoutEnumerator;
    private int mLineCount;
    private bool mScanningLineForRealText;
}
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
