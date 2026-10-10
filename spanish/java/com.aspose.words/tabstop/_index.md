---
title: "TabStop"
linktitle: "TabStop"
second_title: "Aspose.Words para Java"
description: "Representa una única tabulación personalizada en Java."
type: docs
weight: 654
url: /es/java/com.aspose.words/tabstop/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStop implements Cloneable
```

Representa una única tabulación personalizada. El objeto [TabStop](../../com.aspose.words/tabstop/) es un miembro de la colección [TabStopCollection](../../com.aspose.words/tabstopcollection/).

Para obtener más información, visite el artículo de documentación [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

Normalmente, una tabulación especifica una posición donde existe una tabulación. Pero como las tabulaciones pueden heredarse de los estilos padre, puede ser necesario que el objeto hijo defina explícitamente que no hay tabulación en una posición dada. Para eliminar una tabulación heredada en una posición dada, cree un objeto [TabStop](../../com.aspose.words/tabstop/) y establezca [getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) a [TabAlignment.CLEAR](../../com.aspose.words/tabalignment/\#CLEAR).

Para obtener más información, consulte [TabStopCollection](../../com.aspose.words/tabstopcollection/).

 **Examples:** 

Muestra cómo modificar la posición del tabulador derecho en los párrafos relacionados con el TOC.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [TabStop(double position)](#TabStop-double) | Inicializa una nueva instancia de esta clase. |
| [TabStop(double position, int alignment, int leader)](#TabStop-double-int-int) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [equals(TabStop rhs)](#equals-com.aspose.words.TabStop) | Compara con el [TabStop](../../com.aspose.words/tabstop/) especificado. |
| [getAlignment()](#getAlignment) | Obtiene la alineación del texto en esta tabulación. |
| [getLeader()](#getLeader) | Obtiene el tipo de línea de guía mostrada bajo el carácter de tabulación. |
| [getPosition()](#getPosition) | Obtiene la posición de la tabulación en puntos. |
| [hashCode()](#hashCode) |  |
| [isClear()](#isClear) | Devuelve  true  si esta tabulación elimina cualquier tabulación existente en esta posición. |
| [setAlignment(int value)](#setAlignment-int) | Establece la alineación del texto en esta tabulación. |
| [setLeader(int value)](#setLeader-int) | Establece el tipo de línea de guía mostrada bajo el carácter de tabulación. |
### TabStop(double position) {#TabStop-double}
```
public TabStop(double position)
```


Inicializa una nueva instancia de esta clase.

 **Examples:** 

Muestra cómo trabajar con la colección de tabulaciones de un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| posición | double |  |

### TabStop(double position, int alignment, int leader) {#TabStop-double-int-int}
```
public TabStop(double position, int alignment, int leader)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| posición | double |  |
| alineación | int |  |
| líder | int |  |

### equals(TabStop rhs) {#equals-com.aspose.words.TabStop}
```
public boolean equals(TabStop rhs)
```


Compara con el [TabStop](../../com.aspose.words/tabstop/) especificado.

 **Examples:** 

Muestra cómo trabajar con la colección de tabulaciones de un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| rhs | [TabStop](../../com.aspose.words/tabstop/) |  |

**Returns:**
boolean
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Obtiene la alineación del texto en esta tabulación.

 **Examples:** 

Muestra cómo modificar la posición del tabulador derecho en los párrafos relacionados con el TOC.

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
int - La alineación del texto en esta tabulación. El valor devuelto es uno de los constantes de [TabAlignment](../../com.aspose.words/tabalignment/).
### getLeader() {#getLeader}
```
public int getLeader()
```


Obtiene el tipo de línea de guía mostrada bajo el carácter de tabulación.

 **Examples:** 

Muestra cómo modificar la posición del tabulador derecho en los párrafos relacionados con el TOC.

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
int - El tipo de la línea guía mostrada bajo el carácter de tabulación. El valor devuelto es uno de los constantes de [TabLeader](../../com.aspose.words/tableader/).
### getPosition() {#getPosition}
```
public double getPosition()
```


Obtiene la posición de la tabulación en puntos.

 **Examples:** 

Muestra cómo modificar la posición del tabulador derecho en los párrafos relacionados con el TOC.

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
double - La posición de la tabulación en puntos.
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


Devuelve  true  si esta tabulación elimina cualquier tabulación existente en esta posición.

 **Examples:** 

Muestra cómo trabajar con la colección de tabulaciones de un documento.

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
boolean -  true  si esta tabulación elimina cualquier tabulación existente en esta posición.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Establece la alineación del texto en esta tabulación.

 **Examples:** 

Muestra cómo modificar la posición del tabulador derecho en los párrafos relacionados con el TOC.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La alineación del texto en esta tabulación. El valor debe ser uno de los constantes de [TabAlignment](../../com.aspose.words/tabalignment/). |

### setLeader(int value) {#setLeader-int}
```
public void setLeader(int value)
```


Establece el tipo de línea de guía mostrada bajo el carácter de tabulación.

 **Examples:** 

Muestra cómo modificar la posición del tabulador derecho en los párrafos relacionados con el TOC.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El tipo de la línea guía mostrada bajo el carácter de tabulación. El valor debe ser uno de los constantes de [TabLeader](../../com.aspose.words/tableader/). |

