---
title: LoadOptions
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore LoadOptions, progettato per inizializzare senza sforzo una nuova istanza con valori predefiniti per prestazioni ed efficienza ottimali.
type: docs
weight: 10
url: /it/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Inizializza una nuova istanza di questa classe con valori predefiniti.

```csharp
public LoadOptions()
```

## Esempi

Mostra come aprire un documento HTML con immagini da un flusso utilizzando un URI di base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Passare l'URI della cartella base durante il caricamento
    // in modo che sia possibile trovare tutte le immagini con URI relativi nel documento HTML.
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
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)

---

## LoadOptions(*string*) {#constructor_2}

Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato.

```csharp
public LoadOptions(string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | String | La password per aprire un documento crittografato. Può essere`null` o stringa vuota. |

## Esempi

Mostra come caricare un documento Microsoft Word crittografato.

```csharp
Document doc;

// Aspose.Words genera un'eccezione se proviamo ad aprire un documento crittografato senza la relativa password.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Quando si carica un documento di questo tipo, la password viene passata al costruttore del documento tramite un oggetto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Esistono due modi per caricare un documento crittografato con un oggetto LoadOptions.
// 1 - Carica il documento dal file system locale in base al nome file:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Carica il documento da un flusso:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)

---

## LoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

Una scorciatoia per inizializzare una nuova istanza di questa classe con proprietà impostate sui valori specificati.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| loadFormat | LoadFormat | Formato del documento da caricare. |
| password | String | La password per aprire un documento crittografato. Può essere`null` o stringa vuota. |
| baseUri | String | La stringa che verrà utilizzata per risolvere gli URI relativi in assoluti. Può essere`null` o stringa vuota. |

## Esempi

Mostra come salvare una pagina web come file .docx.

```csharp
const string url = "https://products.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // L'URL viene utilizzato nuovamente come baseUri per garantire che tutti i percorsi immagine relativi vengano recuperati correttamente.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Carica il documento HTML dal flusso e passa l'oggetto LoadOptions.
        Document doc = new Document(stream, options);

        // A questo punto possiamo leggere e modificare il contenuto del documento e poi salvarlo nel file system locale.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Mostra come specificare un URI di base quando si apre un documento HTML.

```csharp
// Supponiamo di voler caricare un documento .html che contiene un'immagine collegata da un URI relativo
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
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
