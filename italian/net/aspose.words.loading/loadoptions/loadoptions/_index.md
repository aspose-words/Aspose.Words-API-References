---
title: LoadOptions.LoadOptions
second_title: Aspose.Words per .NET API Reference
description: LoadOptions costruttore. Inizializza una nuova istanza di questa classe con valori predefiniti.
type: docs
weight: 10
url: /it/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Inizializza una nuova istanza di questa classe con valori predefiniti.

```csharp
public LoadOptions()
```

### Esempi

Mostra come aprire un documento HTML con immagini da un flusso utilizzando un URI di base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Passa l'URI della cartella base durante il caricamento
    // in modo che sia possibile trovare eventuali immagini con relativi URI nel documento HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifica che la prima forma del documento contenga un'immagine valida.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../loadoptions/)
* assemblea [Aspose.Words](../../../)

---

## LoadOptions(string) {#constructor_2}

Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato.

```csharp
public LoadOptions(string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | String | La password per aprire un documento crittografato. Può essere`nullo` o stringa vuota. |

### Esempi

Mostra come caricare un documento Microsoft Word crittografato.

```csharp
Document doc;

// Aspose.Words lancia un'eccezione se proviamo ad aprire un documento crittografato senza la sua password.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Quando si carica un documento di questo tipo, la password viene passata al costruttore del documento utilizzando un oggetto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Esistono due modi per caricare un documento crittografato con un oggetto LoadOptions.
// 1 - Carica il documento dal file system locale in base al nome file:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Carica il documento da uno stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../loadoptions/)
* assemblea [Aspose.Words](../../../)

---

## LoadOptions(LoadFormat, string, string) {#constructor_1}

Una scorciatoia per inizializzare una nuova istanza di questa classe con le proprietà impostate sui valori specificati.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| loadFormat | LoadFormat | Il formato del documento da caricare. |
| password | String | La password per aprire un documento crittografato. Può essere`nullo` o stringa vuota. |
| baseUri | String | La stringa che verrà utilizzata per risolvere gli URI relativi in assoluti. Può essere`nullo` o stringa vuota. |

### Esempi

Mostra come salvare una pagina Web come file .docx.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // L'URL viene utilizzato nuovamente come baseUri per garantire che tutti i percorsi relativi alle immagini vengano recuperati correttamente.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Carica il documento HTML dallo stream e passa l'oggetto LoadOptions.
        Document doc = new Document(stream, options);

        // A questo punto possiamo leggere e modificare il contenuto del documento e quindi salvarlo nel file system locale.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Mostra come specificare un URI di base all'apertura di un documento html.

```csharp
// Supponiamo di voler caricare un documento .html che contiene un'immagine collegata da un relativo URI
// mentre l'immagine si trova in una posizione diversa. In tal caso, dovremo risolvere l'URI relativo in uno assoluto.
 // Possiamo fornire un URI di base utilizzando un oggetto HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Sebbene l'immagine fosse danneggiata nell'input .html, il nostro URI di base personalizzato ci ha aiutato a riparare il collegamento.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Questo documento di output visualizzerà l'immagine mancante.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Guarda anche

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../loadoptions/)
* assemblea [Aspose.Words](../../../)


