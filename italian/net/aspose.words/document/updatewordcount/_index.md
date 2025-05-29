---
title: Document.UpdateWordCount
linktitle: UpdateWordCount
articleTitle: UpdateWordCount
second_title: Aspose.Words per .NET
description: Migliora l'efficienza del tuo documento con il metodo UpdateWordCount, garantendo proprietà precise di conteggio delle parole per una migliore modifica e revisione.
type: docs
weight: 850
url: /it/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Aggiorna le proprietà del conteggio delle parole del documento.

```csharp
public void UpdateWordCount()
```

## Osservazioni

`UpdateWordCount` ricalcola e aggiorna le proprietà Caratteri, Parole e Paragrafi in[`BuiltInDocumentProperties`](../builtindocumentproperties/) raccolta di[`Document`](../).

Notare che`UpdateWordCount` non aggiorna le proprietà del numero di linee e pagine. Usa il`UpdateWordCount` sovraccarico e passaggio`VERO` valore come parametro per farlo.

Quando si utilizza una versione di valutazione, la filigrana di valutazione verrà inclusa anche nel conteggio delle parole.

## Esempi

Mostra come aggiornare tutte le etichette degli elenchi in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words non tiene traccia delle metriche dei documenti come queste in tempo reale.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Per ottenere valori accurati per tre di queste proprietà, dovremo aggiornarli manualmente.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Per il conteggio delle righe, dovremo chiamare un overload specifico del metodo di aggiornamento.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## UpdateWordCount(*bool*) {#updatewordcount_1}

Aggiorna le proprietà del conteggio delle parole del documento, facoltativamente aggiorna[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) proprietà.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| updateLinesCount | Boolean | `VERO` se deve essere calcolato il numero di righe nel documento. |

## Osservazioni

Questo metodo ricostruirà il layout di pagina del documento.

## Esempi

Mostra come aggiornare tutte le etichette degli elenchi in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words non tiene traccia delle metriche dei documenti come queste in tempo reale.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Per ottenere valori accurati per tre di queste proprietà, dovremo aggiornarli manualmente.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Per il conteggio delle righe, dovremo chiamare un overload specifico del metodo di aggiornamento.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
