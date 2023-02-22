---
title: Document.UpdateWordCount
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Aggiorna le proprietà del conteggio delle parole del documento.
type: docs
weight: 770
url: /it/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Aggiorna le proprietà del conteggio delle parole del documento.

```csharp
public void UpdateWordCount()
```

### Osservazioni

**Aggiorna Conteggio parole** ricalcola e aggiorna le proprietà di caratteri, parole e paragrafi nel file[`BuiltInDocumentProperties`](../builtindocumentproperties/) raccolta del **Documento**.

Notare che **Aggiorna Conteggio parole** non aggiorna le proprietà del numero di righe e pagine. Utilizzare il`UpdateWordCount` sovraccaricare e passare il valore True come parametro per farlo.

Quando utilizzi una versione di valutazione, anche la filigrana di valutazione verrà inclusa nel conteggio delle parole.

### Esempi

Mostra come aggiornare tutte le etichette degli elenchi in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words non tiene traccia delle metriche del documento come queste in tempo reale.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Per ottenere valori accurati per tre di queste proprietà, dovremo aggiornarle manualmente.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Per il conteggio delle righe, dovremo chiamare un sovraccarico specifico del metodo di aggiornamento.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

---

## UpdateWordCount(bool) {#updatewordcount_1}

Aggiorna le proprietà di conteggio delle parole del documento, facoltativamente aggiorna[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) proprietà.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| updateLinesCount | Boolean | Vero se deve essere calcolato il numero di righe nel documento. |

### Osservazioni

Questo metodo ricostruirà il layout di pagina del documento.

### Esempi

Mostra come aggiornare tutte le etichette degli elenchi in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words non tiene traccia delle metriche del documento come queste in tempo reale.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Per ottenere valori accurati per tre di queste proprietà, dovremo aggiornarle manualmente.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Per il conteggio delle righe, dovremo chiamare un sovraccarico specifico del metodo di aggiornamento.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


