---
title: HtmlLoadOptions.HtmlLoadOptions
second_title: Aspose.Words per .NET API Reference
description: HtmlLoadOptions costruttore. Inizializza una nuova istanza di questa classe con valori predefiniti.
type: docs
weight: 10
url: /it/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Inizializza una nuova istanza di questa classe con valori predefiniti.

```csharp
public HtmlLoadOptions()
```

### Esempi

Mostra come supportare i commenti condizionali durante il caricamento di un documento HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Se il valore è true, prendiamo in considerazione il codice VML durante l'analisi del documento caricato.
loadOptions.SupportVml = supportVml;

// Questo documento contiene un'immagine JPEG all'interno di "<!--[if gte vml 1]>" tag,
// e un'immagine PNG diversa all'interno di "<![if !vml]>" tag.
// Se impostiamo il flag "SupportVml" su "true", Aspose.Words caricherà il JPEG.
// Se impostiamo questo flag su "false", Aspose.Words caricherà solo il PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Guarda anche

* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../htmlloadoptions/)
* assemblea [Aspose.Words](../../../)

---

## HtmlLoadOptions(string) {#constructor_2}

Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato.

```csharp
public HtmlLoadOptions(string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | String | La password per aprire un documento crittografato. Può essere`nullo` o stringa vuota. |

### Esempi

Mostra come crittografare un documento HTML e quindi aprirlo utilizzando una password.

```csharp
// Crea e firma un documento HTML crittografato da un file .docx crittografato.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "HtmlLoadOptions.EncryptedHtml.html";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Per caricare e leggere questo documento, dovremo passarne la decrittazione
// password utilizzando un oggetto HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### Guarda anche

* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../htmlloadoptions/)
* assemblea [Aspose.Words](../../../)

---

## HtmlLoadOptions(LoadFormat, string, string) {#constructor_1}

Una scorciatoia per inizializzare una nuova istanza di questa classe con le proprietà impostate sui valori specificati.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| loadFormat | LoadFormat | Il formato del documento da caricare. |
| password | String | La password per aprire un documento crittografato. Può essere`nullo` o stringa vuota. |
| baseUri | String | La stringa che verrà utilizzata per risolvere gli URI relativi in assoluti. Può essere`nullo` o stringa vuota. |

### Esempi

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
* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../htmlloadoptions/)
* assemblea [Aspose.Words](../../../)


