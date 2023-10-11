---
title: BuiltInDocumentProperties.HyperlinkBase
second_title: Aspose.Words per .NET API Reference
description: BuiltInDocumentProperties proprietà. Specifica la stringa di base utilizzata per valutare i collegamenti ipertestuali relativi in questo documento.
type: docs
weight: 120
url: /it/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Specifica la stringa di base utilizzata per valutare i collegamenti ipertestuali relativi in questo documento.

```csharp
public string HyperlinkBase { get; set; }
```

### Osservazioni

Aspose.Words non utilizza questa proprietà.

### Esempi

Mostra come archiviare la parte base di un collegamento ipertestuale nelle proprietà del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un collegamento ipertestuale relativo a un documento nel file system locale denominato "Document.docx".
// Facendo clic sul collegamento in Microsoft Word si aprirà il documento designato, se disponibile.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Questo collegamento è relativo. Se non è presente "Document.docx" nella stessa cartella
// poiché il documento che contiene questo collegamento, il collegamento verrà interrotto.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Il documento a cui stiamo tentando di collegarci si trova in una directory diversa da quella in cui intendiamo salvare il documento.
 // Potremmo correggere collegamenti come questo inserendo un nome file assoluto in ognuno di essi.
// In alternativa, potremmo fornire un collegamento di base a ogni collegamento ipertestuale con un relativo nome file
 // verrà anteposto al relativo collegamento quando si fa clic su di esso.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Guarda anche

* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../builtindocumentproperties/)
* assemblea [Aspose.Words](../../../)


