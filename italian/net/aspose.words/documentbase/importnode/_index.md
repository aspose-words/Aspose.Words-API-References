---
title: DocumentBase.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words per .NET
description: Importa senza sforzo nodi da altri documenti per migliorare il tuo flusso di lavoro con il metodo ImportNode di DocumentBase. Semplifica la gestione dei tuoi documenti oggi stesso!
type: docs
weight: 110
url: /it/net/aspose.words/documentbase/importnode/
---
## ImportNode(*[Node](../../node/), bool*) {#importnode}

Importa un nodo da un altro documento al documento corrente.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | Node | Il nodo che viene importato. |
| isImportChildren | Boolean | `VERO` per importare tutti i nodi figlio in modo ricorsivo; altrimenti,`falso`. |

### Valore di ritorno

Il nodo clonato che appartiene al documento corrente.

## Osservazioni

Questo metodo utilizza ilUseDestinationStyles opzione per risolvere la formattazione.

L'importazione di un nodo crea una copia del nodo sorgente appartenente al documento importato. Il nodo restituito non ha un nodo padre. Il nodo sorgente non viene modificato o rimosso dal documento originale.

Prima che un nodo da un altro documento possa essere inserito in questo documento, è necessario importarlo. Durante l'importazione, le proprietà specifiche del documento, come i riferimenti a stili ed elenchi, vengono tradotte dal documento originale al documento importato. Dopo l'importazione, il nodo può essere inserito nella posizione appropriata nel documento utilizzando[`InsertBefore`](../../compositenode/insertbefore/) o [`InsertAfter`](../../compositenode/insertafter/).

Se il nodo sorgente appartiene già al documento di destinazione, viene semplicemente creato un clone profondo del nodo sorgente.

## Esempi

Mostra come importare un nodo da un documento a un altro.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Ogni nodo ha un documento padre, che è il documento che contiene il nodo.
// L'inserimento di un nodo in un documento a cui il nodo non appartiene genererà un'eccezione.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => dstDoc.AppendChild(srcDoc.FirstSection));

// Utilizzare il metodo ImportNode per creare una copia di un nodo, che conterrà il documento
// che ha chiamato il metodo ImportNode impostato come nuovo documento proprietario.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// Ora possiamo inserire il nodo nel documento.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### Guarda anche

* class [Node](../../node/)
* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## ImportNode(*[Node](../../node/), bool, [ImportFormatMode](../../importformatmode/)*) {#importnode_1}

Importa un nodo da un altro documento nel documento corrente con un'opzione per controllare la formattazione.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | Node | Il nodo da importare. |
| isImportChildren | Boolean | `VERO` per importare tutti i nodi figlio in modo ricorsivo; altrimenti,`falso`. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione di stile in conflitto. |

### Valore di ritorno

Il nodo clonato e importato. Il nodo appartiene al documento di destinazione, ma non ha un nodo padre.

## Osservazioni

Questo sovraccarico è utile per controllare il modo in cui vengono importati gli stili e la formattazione degli elenchi.

L'importazione di un nodo crea una copia del nodo sorgente appartenente al documento importato. Il nodo restituito non ha un nodo padre. Il nodo sorgente non viene modificato o rimosso dal documento originale.

Prima che un nodo da un altro documento possa essere inserito in questo documento, è necessario importarlo. Durante l'importazione, le proprietà specifiche del documento, come i riferimenti a stili ed elenchi, vengono tradotte dal documento originale al documento importato. Dopo l'importazione, il nodo può essere inserito nella posizione appropriata nel documento utilizzando[`InsertBefore`](../../compositenode/insertbefore/) o [`InsertAfter`](../../compositenode/insertafter/).

Se il nodo sorgente appartiene già al documento di destinazione, viene semplicemente creato un clone profondo del nodo sorgente.

## Esempi

Mostra come importare un nodo dal documento di origine al documento di destinazione con opzioni specifiche.

```csharp
// Crea due documenti e aggiungi uno stile di carattere a ciascun documento.
// Configura gli stili in modo che abbiano lo stesso nome ma una formattazione del testo diversa.
Document srcDoc = new Document();
Style srcStyle = srcDoc.Styles.Add(StyleType.Character, "My style");
srcStyle.Font.Name = "Courier New";
DocumentBuilder srcBuilder = new DocumentBuilder(srcDoc);
srcBuilder.Font.Style = srcStyle;
srcBuilder.Writeln("Source document text.");

Document dstDoc = new Document();
Style dstStyle = dstDoc.Styles.Add(StyleType.Character, "My style");
dstStyle.Font.Name = "Calibri";
DocumentBuilder dstBuilder = new DocumentBuilder(dstDoc);
dstBuilder.Font.Style = dstStyle;
dstBuilder.Writeln("Destination document text.");

// Importa la sezione dal documento di destinazione nel documento di origine, causando una collisione nei nomi degli stili.
// Se utilizziamo stili di destinazione, il testo sorgente importato con lo stesso nome di stile
// poiché il testo di destinazione adotterà lo stile di destinazione.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Se utilizziamo ImportFormatMode.KeepDifferentStyles, lo stile sorgente viene preservato,
// e il conflitto di denominazione viene risolto aggiungendo un suffisso.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Guarda anche

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
