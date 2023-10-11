---
title: DocumentBase.ImportNode
second_title: Aspose.Words per .NET API Reference
description: DocumentBase metodo. Importa un nodo da un altro documento al documento corrente.
type: docs
weight: 100
url: /it/net/aspose.words/documentbase/importnode/
---
## ImportNode(Node, bool) {#importnode}

Importa un nodo da un altro documento al documento corrente.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | Node | Il nodo da importare. |
| isImportChildren | Boolean | `VERO` per importare ricorsivamente tutti i nodi figlio; Altrimenti,`falso`. |

### Valore di ritorno

Il nodo clonato che appartiene al documento corrente.

### Osservazioni

Questo metodo utilizza ilUseDestinationStyles opzione per risolvere la formattazione.

L'importazione di un nodo crea una copia del nodo di origine appartenente al documento di importazione. Il nodo restituito non ha genitore. Il nodo di origine non viene alterato o rimosso dal documento originale.

Prima che un nodo di un altro documento possa essere inserito in questo documento, deve essere importato. Durante l'importazione, le proprietà specifiche del documento come i riferimenti a stili ed elenchi vengono tradotte dal documento originale al documento importato. Dopo che il nodo è stato importato, può essere inserito nella posizione appropriata nel documento utilizzandoNode) o Node).

Se il nodo di origine appartiene già al documento di destinazione, viene semplicemente creato un deep clone del nodo di origine.

### Esempi

Mostra come importare un nodo da un documento a un altro.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Ogni nodo ha un documento genitore, che è il documento che contiene il nodo.
// L'inserimento di un nodo in un documento a cui il nodo non appartiene genererà un'eccezione.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// Utilizza il metodo ImportNode per creare una copia di un nodo, che conterrà il documento
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
* spazio dei nomi [Aspose.Words](../../documentbase/)
* assemblea [Aspose.Words](../../../)

---

## ImportNode(Node, bool, ImportFormatMode) {#importnode_1}

Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | Node | Il nodo da importare. |
| isImportChildren | Boolean | `VERO` per importare ricorsivamente tutti i nodi figlio; Altrimenti,`falso`. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione dello stile in conflitto. |

### Valore di ritorno

Il nodo clonato e importato. Il nodo appartiene al documento di destinazione, ma non ha un genitore.

### Osservazioni

Questo sovraccarico è utile per controllare il modo in cui vengono importati gli stili e la formattazione dell'elenco.

L'importazione di un nodo crea una copia del nodo di origine appartenente al documento di importazione. Il nodo restituito non ha genitore. Il nodo di origine non viene alterato o rimosso dal documento originale.

Prima che un nodo di un altro documento possa essere inserito in questo documento, deve essere importato. Durante l'importazione, le proprietà specifiche del documento come i riferimenti a stili ed elenchi vengono tradotte dal documento originale al documento importato. Dopo che il nodo è stato importato, può essere inserito nella posizione appropriata nel documento utilizzandoNode) o Node).

Se il nodo di origine appartiene già al documento di destinazione, viene semplicemente creato un deep clone del nodo di origine.

### Esempi

Mostra come importare il nodo dal documento di origine al documento di destinazione con opzioni specifiche.

```csharp
// Crea due documenti e aggiungi uno stile di carattere a ciascun documento.
// Configura gli stili in modo che abbiano lo stesso nome, ma una formattazione del testo diversa.
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

// Importa la sezione dal documento di destinazione al documento di origine, causando una collisione tra i nomi di stile.
// Se utilizziamo gli stili di destinazione, il testo di origine importato avrà lo stesso nome di stile
// poiché il testo di destinazione adotterà lo stile di destinazione.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Se utilizziamo ImportFormatMode.KeepDifferentStyles, lo stile di origine viene preservato,
// e il conflitto di nomi si risolve aggiungendo un suffisso.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Guarda anche

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../documentbase/)
* assemblea [Aspose.Words](../../../)


