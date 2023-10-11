---
title: SaveOptions.UpdateLastPrintedProperty
second_title: Aspose.Words per .NET API Reference
description: SaveOptions proprietà. Ottiene o imposta un valore che determina se ilLastPrinted la proprietà viene aggiornata prima del salvataggio.
type: docs
weight: 170
url: /it/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Ottiene o imposta un valore che determina se il[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

### Esempi

Mostra come aggiornare la proprietà "CreatedTime" di un documento durante il salvataggio.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.CreatedTime = new DateTime(2019, 12, 20);

// Questo flag determina se l'ora creata, che è una proprietà incorporata, viene aggiornata.
// In tal caso, la data dell'operazione di salvataggio più recente del documento
// con questo oggetto SaveOptions passato come parametro viene utilizzato come orario creato.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Apre il documento salvato, quindi verifica il valore della proprietà.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

Assert.AreNotEqual(isUpdateCreatedTimeProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.CreatedTime);
```

Mostra come aggiornare la proprietà "Ultima stampa" di un documento durante il salvataggio.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.LastPrinted = new DateTime(2019, 12, 20);

// Questo flag determina se l'ultima data stampata, che è una proprietà incorporata, viene aggiornata.
// In tal caso, la data dell'operazione di salvataggio più recente del documento
// con questo oggetto SaveOptions passato come parametro viene utilizzata come data di stampa.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// In Microsoft Word 2003, questa proprietà può essere trovata tramite File -> Proprietà -> Statistiche -> Stampato.
// Può anche essere visualizzato nel corpo del documento utilizzando un campo PRINTDATE.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Apre il documento salvato, quindi verifica il valore della proprietà.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

Assert.AreNotEqual(isUpdateLastPrintedProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.LastPrinted);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../saveoptions/)
* assemblea [Aspose.Words](../../../)


