---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words per .NET
description: Ottimizza la gestione dei documenti con SaveOptions UpdateLastPrintedProperty. Controlla gli aggiornamenti di LastPrinted per un salvataggio efficiente e un flusso di lavoro migliorato.
type: docs
weight: 180
url: /it/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Ottiene o imposta un valore che determina se il[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Esempi

Mostra come aggiornare la proprietà "Ultima stampa" di un documento durante il salvataggio.

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// Questo flag determina se l'ultima data stampata, che è una proprietà incorporata, viene aggiornata.
// In tal caso, la data dell'operazione di salvataggio più recente del documento
// con questo oggetto SaveOptions passato come parametro viene utilizzato come data di stampa.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// In Microsoft Word 2003, questa proprietà può essere trovata tramite File -> Proprietà -> Statistiche -> Stampato.
// Può anche essere visualizzato nel corpo del documento utilizzando un campo PRINTDATE.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Aprire il documento salvato, quindi verificare il valore della proprietà.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.AreNotEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
else
    Assert.AreEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
