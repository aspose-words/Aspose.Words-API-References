---
title: BuiltInDocumentProperties.LinksUpToDate
second_title: Referencia de API de Aspose.Words para .NET
description: BuiltInDocumentProperties propiedad. Indica si los hipervínculos de un documento están actualizados.
type: docs
weight: 190
url: /es/net/aspose.words.properties/builtindocumentproperties/linksuptodate/
---
## BuiltInDocumentProperties.LinksUpToDate property

Indica si los hipervínculos de un documento están actualizados.

```csharp
public bool LinksUpToDate { get; set; }
```

### Observaciones

Aspose.Words no actualiza esta propiedad.

### Ejemplos

Muestra cómo trabajar con las propiedades del documento en la categoría "Contenido".

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Mediante el uso de propiedades integradas,
    // podemos tratar las estadísticas del documento, como el recuento de palabras/páginas/caracteres, como metadatos que se pueden consultar sin abrir el documento
    // Se accede a estas propiedades haciendo clic derecho en el archivo en el Explorador de Windows y navegando a Propiedades > Detalles > Contenido
    // Si queremos mostrar estos datos dentro del documento, podemos usar campos como NUMPAGES, NUMWORDS, NUMCHARS, etc.
    // Además, estos valores también se pueden ver en Microsoft Word navegando por Archivo > Propiedades > Propiedades avanzadas > Estadísticas
    // Recuento de páginas: la propiedad PageCount muestra el recuento de páginas en tiempo real y su valor se puede asignar a la propiedad Pages

    // La propiedad "Páginas" almacena el número de páginas del documento. 
    Assert.AreEqual(6, properties.Pages);

    // Las propiedades integradas "Words", "Characters" y "CharactersWithSpaces" también muestran varias estadísticas de documentos,
    // pero necesitamos llamar al método "UpdateWordCount" en todo el documento antes de que podamos esperar que contengan valores precisos.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Cuente el número de líneas en el documento y luego asigne el resultado a la propiedad integrada "Líneas".
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Asigne el número de nodos de Párrafo en el documento a la propiedad integrada "Párrafos".
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Obtenga una estimación del tamaño de archivo de nuestro documento a través de la propiedad integrada "Bytes".
    Assert.AreEqual(20310, properties.Bytes);

    // Establezca una plantilla diferente para nuestro documento y luego actualice la propiedad integrada "Plantilla" manualmente para reflejar este cambio.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" es una propiedad integrada descriptiva.
    properties.ContentStatus = "Draft";

    // Al guardar, la propiedad integrada "ContentType" contendrá el tipo MIME del formato de guardado de salida.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Si el documento contiene enlaces y todos están actualizados, podemos establecer la propiedad "LinksUpToDate" en "true".
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Cuenta las líneas de un documento.
/// Atraviesa el árbol de entidades de diseño del documento durante la construcción,
/// entidades de conteo del tipo "Línea" que también contienen texto real.
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
* espacio de nombres [Aspose.Words.Properties](../../builtindocumentproperties/)
* asamblea [Aspose.Words](../../../)


