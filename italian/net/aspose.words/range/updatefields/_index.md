---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti senza sforzo con il metodo Range UpdateFields, aggiornando i valori dei campi in modo rapido ed efficiente per una maggiore precisione.
type: docs
weight: 130
url: /it/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Aggiorna i valori dei campi del documento in questo intervallo.

```csharp
public void UpdateFields()
```

## Osservazioni

Quando si apre, si modifica e si salva un documento, Aspose.Words non aggiorna automaticamente i campi, ma li mantiene intatti. Pertanto, in genere si desidera chiamare questo metodo prima di salvare se si è modificato il documento a livello di codice e si desidera assicurarsi che i valori dei campi corretti (calcolati) vengano visualizzati nel documento salvato.

Non è necessario aggiornare i campi dopo aver eseguito una stampa unione, perché la stampa unione è un tipo di aggiornamento di campo e aggiorna automaticamente tutti i campi nel documento.

Questo metodo non aggiorna tutti i tipi di campo. Per un elenco dettagliato dei tipi di campo supportati, consultare la Guida per i programmatori.

Questo metodo non aggiorna i campi correlati agli algoritmi di layout di pagina (ad esempio PAGE, PAGES, PAGEREF). I campi correlati al layout di pagina vengono aggiornati quando si esegue il rendering di un documento o si chiama[`UpdatePageLayout`](../../document/updatepagelayout/).

Per aggiornare i campi nell'intero documento utilizzare[`UpdateFields`](../../document/updatefields/).

## Esempi

Mostra come aggiornare tutti i campi in un intervallo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// I campi DOCPROPERTY soprastanti visualizzeranno il valore di questa proprietà del documento incorporata.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Se aggiorniamo il valore di una proprietà del documento, dovremo aggiornare tutti i campi DOCPROPERTY per visualizzarlo.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// Aggiorna tutti i campi che rientrano nell'intervallo della prima sezione.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Guarda anche

* class [Range](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
