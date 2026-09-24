---
title: "TabStopCollection"
linktitle: "TabStopCollection"
second_title: "Aspose.Words para Java"
description: "Una colección de objetos TabStop que representan tabulaciones personalizadas para un párrafo o un estilo en Java."
type: docs
weight: 655
url: /es/java/com.aspose.words/tabstopcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStopCollection extends InternableComplexAttr implements Cloneable
```

Una colección de objetos [TabStop](../../com.aspose.words/tabstop/) que representan tabulaciones personalizadas para un párrafo o un estilo.

Para obtener más información, visite el artículo de documentación [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

En los documentos de Microsoft Word, una tabulación puede definirse en las propiedades de un estilo de párrafo o directamente en las propiedades de un párrafo. Un estilo puede basarse en otro estilo. Por lo tanto, el conjunto completo de tabulaciones para un objeto dado es una combinación de las tabulaciones definidas directamente en este objeto y las tabulaciones heredadas de los estilos padre.

En Aspose.Words, cuando se obtiene una [TabStopCollection](../../com.aspose.words/tabstopcollection/) para un párrafo o un estilo, contiene solo las tabulaciones personalizadas definidas directamente para ese párrafo o estilo. La colección no incluye las tabulaciones definidas en los estilos padre ni las tabulaciones predeterminadas.

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


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Métodos

| Método | Descripción |
| --- | --- |
| [add(TabStop tabStop)](#add-com.aspose.words.TabStop) | Agrega o reemplaza una tabulación en la colección. |
| [add(double position, int alignment, int leader)](#add-double-int-int) |  |
| [after(double position)](#after-double) | Obtiene la primera tabulación a la derecha de la posición especificada. |
| [before(double position)](#before-double) | Obtiene la primera tabulación a la izquierda de la posición especificada. |
| [clear()](#clear) | Elimina todas las posiciones de tabulación. |
| [equals(TabStopCollection rhs)](#equals-com.aspose.words.TabStopCollection) | Determina si la [TabStopCollection](../../com.aspose.words/tabstopcollection/) especificada es igual en valor a la [TabStopCollection](../../com.aspose.words/tabstopcollection/) actual. |
| [equals(Object obj)](#equals-java.lang.Object) | Determina si el objeto especificado es igual en valor al objeto actual. |
| [get(double position)](#get-double) | Obtiene una tabulación en la posición especificada. |
| [get(int index)](#get-int) | Recupera una tabulación de la colección. |
| [getCount()](#getCount) | Obtiene el número de tabulaciones en la colección. |
| [getIndexByPosition(double position)](#getIndexByPosition-double) | Obtiene el índice de una tabulación con la posición especificada en puntos. |
| [getPositionByIndex(int index)](#getPositionByIndex-int) | Obtiene la posición (en puntos) de la tabulación en el índice especificado. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [removeByIndex(int index)](#removeByIndex-int) | Elimina una tabulación en el índice especificado de la colección. |
| [removeByPosition(double position)](#removeByPosition-double) | Elimina una tabulación en la posición especificada de la colección. |
### add(TabStop tabStop) {#add-com.aspose.words.TabStop}
```
public void add(TabStop tabStop)
```


Agrega o reemplaza una tabulación en la colección.

 **Remarks:** 

Si ya existe una tabulación en la posición especificada, se reemplaza.

 **Examples:** 

Muestra cómo agregar tabulaciones personalizadas a un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tabStop | [TabStop](../../com.aspose.words/tabstop/) | Un objeto de tabulación para agregar. |

### add(double position, int alignment, int leader) {#add-double-int-int}
```
public void add(double position, int alignment, int leader)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| posición | double |  |
| alineación | int |  |
| líder | int |  |

### after(double position) {#after-double}
```
public TabStop after(double position)
```


Obtiene la primera tabulación a la derecha de la posición especificada.

 **Remarks:** 

Omite las tabulaciones con [TabStop.getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) configuradas a [TabAlignment.BAR](../../com.aspose.words/tabalignment/\#BAR).

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
| posición | double | La posición de referencia (en puntos). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop object or  null  if a suitable tab stop was not found.
### before(double position) {#before-double}
```
public TabStop before(double position)
```


Obtiene la primera tabulación a la izquierda de la posición especificada.

 **Remarks:** 

Omite las tabulaciones con [TabStop.getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) configuradas a [TabAlignment.BAR](../../com.aspose.words/tabalignment/\#BAR).

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
| posición | double | La posición de referencia (en puntos). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop object or  null  if a suitable tab stop was not found.
### clear() {#clear}
```
public void clear()
```


Elimina todas las posiciones de tabulación.

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

### equals(TabStopCollection rhs) {#equals-com.aspose.words.TabStopCollection}
```
public boolean equals(TabStopCollection rhs)
```


Determina si la [TabStopCollection](../../com.aspose.words/tabstopcollection/) especificada es igual en valor a la [TabStopCollection](../../com.aspose.words/tabstopcollection/) actual.

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
| rhs | [TabStopCollection](../../com.aspose.words/tabstopcollection/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determina si el objeto especificado es igual en valor al objeto actual.

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
| obj | java.lang.Object |  |

**Returns:**
boolean
### get(double position) {#get-double}
```
public TabStop get(double position)
```


Obtiene una tabulación en la posición especificada.

 **Remarks:** 

Devuelve  null  si no se encuentra ninguna tabulación en la posición especificada.

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
| posición | double | La posición (en puntos) de la tabulación. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop at the specified position.
### get(int index) {#get-int}
```
public TabStop get(int index)
```


Recupera una tabulación de la colección.  Obtiene una tabulación en el índice dado.

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
| índice | int | Un índice dentro de la colección de tabulaciones. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - The corresponding [TabStop](../../com.aspose.words/tabstop/) value.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de tabulaciones en la colección.

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
int - El número de tabulaciones en la colección.
### getIndexByPosition(double position) {#getIndexByPosition-double}
```
public int getIndexByPosition(double position)
```


Obtiene el índice de una tabulación con la posición especificada en puntos.

 **Examples:** 

Muestra cómo buscar una posición para ver si existe una tabulación allí y obtener su índice.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| posición | double |  |

**Returns:**
int
### getPositionByIndex(int index) {#getPositionByIndex-int}
```
public double getPositionByIndex(int index)
```


Obtiene la posición (en puntos) de la tabulación en el índice especificado.

 **Examples:** 

Muestra cómo encontrar una tabulación por su índice y verificar su posición.

```

 Document doc = new Document();
 TabStopCollection tabStops = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getTabStops();

 tabStops.add(ConvertUtil.millimeterToPoint(30.0), TabAlignment.LEFT, TabLeader.DASHES);
 tabStops.add(ConvertUtil.millimeterToPoint(60.0), TabAlignment.LEFT, TabLeader.DASHES);

 // Verify the position of the second tab stop in the collection.
 Assert.assertEquals(ConvertUtil.millimeterToPoint(60.0), tabStops.getPositionByIndex(1), 0.1d);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Un índice dentro de la colección de tabulaciones. |

**Returns:**
double - La posición de la tabulación.
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


Elimina una tabulación en el índice especificado de la colección.

 **Examples:** 

Muestra cómo seleccionar una tabulación en un documento por su índice y eliminarla.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Un índice dentro de la colección de tabulaciones. |

### removeByPosition(double position) {#removeByPosition-double}
```
public void removeByPosition(double position)
```


Elimina una tabulación en la posición especificada de la colección.

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
| posición | double | La posición (en puntos) del tabulador a eliminar. |

