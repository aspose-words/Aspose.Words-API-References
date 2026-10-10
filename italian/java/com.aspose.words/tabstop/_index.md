---
title: "TabStop"
linktitle: "TabStop"
second_title: "Aspose.Words per Java"
description: "Rappresenta una singola tabulazione personalizzata in Java."
type: docs
weight: 654
url: /it/java/com.aspose.words/tabstop/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStop implements Cloneable
```

Rappresenta una singola tabulazione personalizzata. L'oggetto [TabStop](../../com.aspose.words/tabstop/) è un membro della collezione [TabStopCollection](../../com.aspose.words/tabstopcollection/).

Per saperne di più, visita l'articolo della documentazione [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

Normalmente, una tabulazione specifica una posizione in cui esiste una tabulazione. Tuttavia, poiché le tabulazioni possono essere ereditate dagli stili genitore, potrebbe essere necessario che l'oggetto figlio definisca esplicitamente che non esiste alcuna tabulazione in una data posizione. Per cancellare una tabulazione ereditata in una data posizione, crea un oggetto [TabStop](../../com.aspose.words/tabstop/) e imposta [getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) su [TabAlignment.CLEAR](../../com.aspose.words/tabalignment/\#CLEAR).

Per ulteriori informazioni, vedi [TabStopCollection](../../com.aspose.words/tabstopcollection/).

 **Examples:** 

Mostra come modificare la posizione della tabulazione destra nei paragrafi correlati all'indice.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [TabStop(double position)](#TabStop-double) | Inizializza una nuova istanza di questa classe. |
| [TabStop(double position, int alignment, int leader)](#TabStop-double-int-int) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [equals(TabStop rhs)](#equals-com.aspose.words.TabStop) | Confronta con il [TabStop](../../com.aspose.words/tabstop/) specificato. |
| [getAlignment()](#getAlignment) | Ottiene l'allineamento del testo in questa tabulazione. |
| [getLeader()](#getLeader) | Ottiene il tipo della linea guida visualizzata sotto il carattere di tabulazione. |
| [getPosition()](#getPosition) | Ottiene la posizione della tabulazione in punti. |
| [hashCode()](#hashCode) |  |
| [isClear()](#isClear) | Restituisce  true  se questa tabulazione cancella eventuali tabulazioni esistenti in questa posizione. |
| [setAlignment(int value)](#setAlignment-int) | Imposta l'allineamento del testo in questa tabulazione. |
| [setLeader(int value)](#setLeader-int) | Imposta il tipo della linea guida visualizzata sotto il carattere di tabulazione. |
### TabStop(double position) {#TabStop-double}
```
public TabStop(double position)
```


Inizializza una nuova istanza di questa classe.

 **Examples:** 

Mostra come lavorare con la raccolta di tabulazioni di un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| posizione | double |  |

### TabStop(double position, int alignment, int leader) {#TabStop-double-int-int}
```
public TabStop(double position, int alignment, int leader)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| posizione | double |  |
| allineamento | int |  |
| leader | int |  |

### equals(TabStop rhs) {#equals-com.aspose.words.TabStop}
```
public boolean equals(TabStop rhs)
```


Confronta con il [TabStop](../../com.aspose.words/tabstop/) specificato.

 **Examples:** 

Mostra come lavorare con la raccolta di tabulazioni di un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| rhs | [TabStop](../../com.aspose.words/tabstop/) |  |

**Returns:**
boolean
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Ottiene l'allineamento del testo in questa tabulazione.

 **Examples:** 

Mostra come modificare la posizione della tabulazione destra nei paragrafi correlati all'indice.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
int - L'allineamento del testo a questa tabulazione. Il valore restituito è una delle costanti [TabAlignment](../../com.aspose.words/tabalignment/).
### getLeader() {#getLeader}
```
public int getLeader()
```


Ottiene il tipo della linea guida visualizzata sotto il carattere di tabulazione.

 **Examples:** 

Mostra come modificare la posizione della tabulazione destra nei paragrafi correlati all'indice.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
int - Il tipo della linea guida visualizzata sotto il carattere di tabulazione. Il valore restituito è una delle costanti [TabLeader](../../com.aspose.words/tableader/).
### getPosition() {#getPosition}
```
public double getPosition()
```


Ottiene la posizione della tabulazione in punti.

 **Examples:** 

Mostra come modificare la posizione della tabulazione destra nei paragrafi correlati all'indice.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
double - La posizione della tabulazione in punti.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isClear() {#isClear}
```
public boolean isClear()
```


Restituisce  true  se questa tabulazione cancella eventuali tabulazioni esistenti in questa posizione.

 **Examples:** 

Mostra come lavorare con la raccolta di tabulazioni di un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Returns:**
boolean -  true  se questa tabulazione elimina eventuali tabulazioni esistenti in questa posizione.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Imposta l'allineamento del testo in questa tabulazione.

 **Examples:** 

Mostra come modificare la posizione della tabulazione destra nei paragrafi correlati all'indice.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | L'allineamento del testo a questa tabulazione. Il valore deve essere una delle costanti [TabAlignment](../../com.aspose.words/tabalignment/). |

### setLeader(int value) {#setLeader-int}
```
public void setLeader(int value)
```


Imposta il tipo della linea guida visualizzata sotto il carattere di tabulazione.

 **Examples:** 

Mostra come modificare la posizione della tabulazione destra nei paragrafi correlati all'indice.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il tipo della linea guida visualizzata sotto il carattere di tabulazione. Il valore deve essere una delle costanti [TabLeader](../../com.aspose.words/tableader/). |

