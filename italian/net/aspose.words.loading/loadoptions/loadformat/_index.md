---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà LoadFormat di LoadOptions per specificare facilmente i formati dei documenti. Ottimizza il caricamento con l'impostazione predefinita Auto per prestazioni impeccabili.
type: docs
weight: 90
url: /it/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Specifica il formato del documento da caricare. Il valore predefinito èAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Osservazioni

Si consiglia di specificare ilAuto valore e lasciare che Aspose.Words rilevi automaticamente il formato del file. Se si conosce il formato del documento che si sta per caricare, è possibile specificare esplicitamente il formato. Questo ridurrà leggermente il tempo di caricamento, dovuto al sovraccarico associato al rilevamento automatico del formato. Se si specifica un formato di caricamento esplicito e questo risulta errato, verrà richiamato il rilevamento automatico e verrà effettuato un secondo tentativo di caricamento del file.

## Esempi

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
