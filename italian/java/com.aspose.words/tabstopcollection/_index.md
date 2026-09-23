---
title: "TabStopCollection"
linktitle: "TabStopCollection"
second_title: "Aspose.Words per Java"
description: "Una raccolta di oggetti TabStop che rappresentano tabulazioni personalizzate per un paragrafo o uno stile in Java."
type: docs
weight: 655
url: /it/java/com.aspose.words/tabstopcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStopCollection extends InternableComplexAttr implements Cloneable
```

Una raccolta di oggetti [TabStop](../../com.aspose.words/tabstop/) che rappresentano tabulazioni personalizzate per un paragrafo o uno stile.

Per saperne di più, visita l'articolo della documentazione [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

Nei documenti Microsoft Word, una tabulazione può essere definita nelle proprietà di uno stile di paragrafo o direttamente nelle proprietà di un paragrafo. Uno stile può basarsi su un altro stile. Pertanto, l'insieme completo di tabulazioni per un determinato oggetto è una combinazione di tabulazioni definite direttamente su questo oggetto e di tabulazioni ereditate dagli stili genitore.

In Aspose.Words, quando si ottiene una [TabStopCollection](../../com.aspose.words/tabstopcollection/) per un paragrafo o uno stile, contiene solo le tabulazioni personalizzate definite direttamente per quel paragrafo o stile. La raccolta non include le tabulazioni definite negli stili genitore o le tabulazioni predefinite.

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


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(TabStop tabStop)](#add-com.aspose.words.TabStop) | Aggiunge o sostituisce una tabulazione nella raccolta. |
| [add(double position, int alignment, int leader)](#add-double-int-int) |  |
| [after(double position)](#after-double) | Ottiene la prima tabulazione a destra della posizione specificata. |
| [before(double position)](#before-double) | Ottiene la prima tabulazione a sinistra della posizione specificata. |
| [clear()](#clear) | Elimina tutte le posizioni delle tabulazioni. |
| [equals(TabStopCollection rhs)](#equals-com.aspose.words.TabStopCollection) | Determina se la [TabStopCollection](../../com.aspose.words/tabstopcollection/) specificata è uguale in valore alla [TabStopCollection](../../com.aspose.words/tabstopcollection/) corrente. |
| [equals(Object obj)](#equals-java.lang.Object) | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get(double position)](#get-double) | Ottiene una tabulazione nella posizione specificata. |
| [get(int index)](#get-int) | Recupera una tabulazione dalla collezione. |
| [getCount()](#getCount) | Ottiene il numero di tabulazioni nella collezione. |
| [getIndexByPosition(double position)](#getIndexByPosition-double) | Ottiene l'indice di una tabulazione con la posizione specificata in punti. |
| [getPositionByIndex(int index)](#getPositionByIndex-int) | Ottiene la posizione (in punti) della tabulazione all'indice specificato. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [removeByIndex(int index)](#removeByIndex-int) | Rimuove una tabulazione all'indice specificato dalla collezione. |
| [removeByPosition(double position)](#removeByPosition-double) | Rimuove una tabulazione nella posizione specificata dalla collezione. |
### add(TabStop tabStop) {#add-com.aspose.words.TabStop}
```
public void add(TabStop tabStop)
```


Aggiunge o sostituisce una tabulazione nella raccolta.

 **Remarks:** 

Se una tabulazione esiste già nella posizione specificata, viene sostituita.

 **Examples:** 

Mostra come aggiungere tabulazioni personalizzate a un documento.

```

 Document doc = new Document();
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Below are two ways of adding tab stops to a paragraph's collection of tab stops via the "ParagraphFormat" property.
 // 1 -  Create a "TabStop" object, and then add it to the collection:
 TabStop tabStop = new TabStop(ConvertUtil.inchToPoint(3.0), TabAlignment.LEFT, TabLeader.DASHES);
 paragraph.getParagraphFormat().getTabStops().add(tabStop);

 // 2 -  Pass the values for properties of a new tab stop to the "Add" method:
 paragraph.getParagraphFormat().getTabStops().add(ConvertUtil.millimeterToPoint(100.0), TabAlignment.LEFT,
         TabLeader.DASHES);

 // Add tab stops at 5 cm to all paragraphs.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     para.getParagraphFormat().getTabStops().add(ConvertUtil.millimeterToPoint(50.0), TabAlignment.LEFT,
             TabLeader.DASHES);
 }

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

 doc.save(getArtifactsDir() + "TabStopCollection.AddTabStops.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tabStop | [TabStop](../../com.aspose.words/tabstop/) | Un oggetto tabulazione da aggiungere. |

### add(double position, int alignment, int leader) {#add-double-int-int}
```
public void add(double position, int alignment, int leader)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| posizione | double |  |
| allineamento | int |  |
| leader | int |  |

### after(double position) {#after-double}
```
public TabStop after(double position)
```


Ottiene la prima tabulazione a destra della posizione specificata.

 **Remarks:** 

Ignora le tabulazioni con [TabStop.getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) impostate su [TabAlignment.BAR](../../com.aspose.words/tabalignment/\#BAR).

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
| posizione | double | La posizione di riferimento (in punti). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop object or  null  if a suitable tab stop was not found.
### before(double position) {#before-double}
```
public TabStop before(double position)
```


Ottiene la prima tabulazione a sinistra della posizione specificata.

 **Remarks:** 

Ignora le tabulazioni con [TabStop.getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) impostate su [TabAlignment.BAR](../../com.aspose.words/tabalignment/\#BAR).

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
| posizione | double | La posizione di riferimento (in punti). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop object or  null  if a suitable tab stop was not found.
### clear() {#clear}
```
public void clear()
```


Elimina tutte le posizioni delle tabulazioni.

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

### equals(TabStopCollection rhs) {#equals-com.aspose.words.TabStopCollection}
```
public boolean equals(TabStopCollection rhs)
```


Determina se la [TabStopCollection](../../com.aspose.words/tabstopcollection/) specificata è uguale in valore alla [TabStopCollection](../../com.aspose.words/tabstopcollection/) corrente.

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
| rhs | [TabStopCollection](../../com.aspose.words/tabstopcollection/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determina se l'oggetto specificato è uguale in valore all'oggetto corrente.

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
| obj | java.lang.Object |  |

**Returns:**
boolean
### get(double position) {#get-double}
```
public TabStop get(double position)
```


Ottiene una tabulazione nella posizione specificata.

 **Remarks:** 

Restituisce  null  se non viene trovata alcuna tabulazione nella posizione specificata.

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
| posizione | double | La posizione (in punti) della tabulazione. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop at the specified position.
### get(int index) {#get-int}
```
public TabStop get(int index)
```


Recupera una tabulazione dalla collezione.  Ottiene una tabulazione all'indice fornito.

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
| indice | int | Un indice nella collezione di tabulazioni. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - The corresponding [TabStop](../../com.aspose.words/tabstop/) value.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di tabulazioni nella collezione.

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
int - Il numero di tabulazioni nella collezione.
### getIndexByPosition(double position) {#getIndexByPosition-double}
```
public int getIndexByPosition(double position)
```


Ottiene l'indice di una tabulazione con la posizione specificata in punti.

 **Examples:** 

Mostra come verificare una posizione per vedere se esiste una tabulazione e ottenere il suo indice.

```

 Document doc = new Document();
 TabStopCollection tabStops = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getTabStops();

 // Add a tab stop at a position of 30mm.
 tabStops.add(ConvertUtil.millimeterToPoint(30.0), TabAlignment.LEFT, TabLeader.DASHES);

 // A result of "0" returned by "GetIndexByPosition" confirms that a tab stop
 // at 30mm exists in this collection, and it is at index 0.
 Assert.assertEquals(0, tabStops.getIndexByPosition(ConvertUtil.millimeterToPoint(30.0)));

 // A "-1" returned by "GetIndexByPosition" confirms that
 // there is no tab stop in this collection with a position of 60mm.
 Assert.assertEquals(-1, tabStops.getIndexByPosition(ConvertUtil.millimeterToPoint(60.0)));
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| posizione | double |  |

**Returns:**
int
### getPositionByIndex(int index) {#getPositionByIndex-int}
```
public double getPositionByIndex(int index)
```


Ottiene la posizione (in punti) della tabulazione all'indice specificato.

 **Examples:** 

Mostra come trovare una tabulazione per indice e verificare la sua posizione.

```

 Document doc = new Document();
 TabStopCollection tabStops = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getTabStops();

 tabStops.add(ConvertUtil.millimeterToPoint(30.0), TabAlignment.LEFT, TabLeader.DASHES);
 tabStops.add(ConvertUtil.millimeterToPoint(60.0), TabAlignment.LEFT, TabLeader.DASHES);

 // Verify the position of the second tab stop in the collection.
 Assert.assertEquals(ConvertUtil.millimeterToPoint(60.0), tabStops.getPositionByIndex(1), 0.1d);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Un indice nella collezione di tabulazioni. |

**Returns:**
double - La posizione della tabulazione.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### removeByIndex(int index) {#removeByIndex-int}
```
public void removeByIndex(int index)
```


Rimuove una tabulazione all'indice specificato dalla collezione.

 **Examples:** 

Mostra come selezionare una tabulazione in un documento per indice e rimuoverla.

```

 Document doc = new Document();
 TabStopCollection tabStops = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getTabStops();

 tabStops.add(ConvertUtil.millimeterToPoint(30.0), TabAlignment.LEFT, TabLeader.DASHES);
 tabStops.add(ConvertUtil.millimeterToPoint(60.0), TabAlignment.LEFT, TabLeader.DASHES);

 Assert.assertEquals(2, tabStops.getCount());

 // Remove the first tab stop.
 tabStops.removeByIndex(0);

 Assert.assertEquals(1, tabStops.getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.RemoveByIndex.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Un indice nella collezione di tabulazioni. |

### removeByPosition(double position) {#removeByPosition-double}
```
public void removeByPosition(double position)
```


Rimuove una tabulazione nella posizione specificata dalla collezione.

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
| posizione | double | La posizione (in punti) della tabulazione da rimuovere. |

