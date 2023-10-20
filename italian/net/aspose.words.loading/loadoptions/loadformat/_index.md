---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words per .NET
description: LoadOptions LoadFormat proprietà. Specifica il formato del documento da caricare. Il valore predefinito èAuto  in C#.
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

Si consiglia di specificare ilAuto valore e lascia che Aspose.Words rilevi il formato del file automaticamente. Se conosci il formato del documento che stai per caricare, puoi specificare format esplicitamente e questo ridurrà leggermente il tempo di caricamento a causa del sovraccarico associato al rilevamento automatico del formato. Se specifichi un formato di caricamento esplicito e cambierà che sia sbagliato, verrà richiamato il rilevamento automatico e verrà effettuato un secondo tentativo di caricare il file.

## Esempi

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
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
