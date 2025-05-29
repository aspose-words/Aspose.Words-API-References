---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words per .NET
description: Scopri la proprietà HyperlinkBase di BuiltInDocumentProperties per ottimizzare i collegamenti ipertestuali relativi nei tuoi documenti, per una navigazione fluida e un'esperienza utente migliorata.
type: docs
weight: 120
url: /it/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Specifica la stringa di base utilizzata per valutare i collegamenti ipertestuali relativi in questo documento.

```csharp
public string HyperlinkBase { get; set; }
```

## Osservazioni

Aspose.Words non utilizza questa proprietà.

## Esempi

Mostra come memorizzare la parte base di un collegamento ipertestuale nelle proprietà del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un collegamento ipertestuale relativo a un documento nel file system locale denominato "Document.docx".
// Facendo clic sul collegamento in Microsoft Word si aprirà il documento designato, se disponibile.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Questo collegamento è relativo. Se non c'è "Document.docx" nella stessa cartella
// poiché il documento che contiene questo collegamento sarà interrotto.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Il documento a cui stiamo cercando di collegarci si trova in una directory diversa da quella in cui prevediamo di salvarlo.
 // Potremmo correggere collegamenti come questo inserendo un nome file assoluto in ciascuno di essi.
// In alternativa, potremmo fornire un collegamento di base in cui ogni collegamento ipertestuale con un nome file relativo
 // verrà aggiunto all'inizio del collegamento quando cliccheremo su di esso.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Guarda anche

* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
