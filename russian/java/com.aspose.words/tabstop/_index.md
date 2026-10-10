---
title: "TabStop"
linktitle: "TabStop"
second_title: "Aspose.Words для Java"
description: "Представляет одну пользовательскую табуляцию в Java."
type: docs
weight: 654
url: /ru/java/com.aspose.words/tabstop/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStop implements Cloneable
```

Представляет одну пользовательскую табуляцию. Объект [TabStop](../../com.aspose.words/tabstop/) является членом коллекции [TabStopCollection](../../com.aspose.words/tabstopcollection/).

Чтобы узнать больше, посетите статью документации [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

Обычно табуляция задаёт позицию, где она существует. Но поскольку табуляции могут наследоваться от стилей‑родителей, может потребоваться явно указать для дочернего объекта, что в заданной позиции нет табуляции. Чтобы очистить унаследованную табуляцию в заданной позиции, создайте объект [TabStop](../../com.aspose.words/tabstop/) и установите [getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) в значение [TabAlignment.CLEAR](../../com.aspose.words/tabalignment/\#CLEAR).

Для получения дополнительной информации см. [TabStopCollection](../../com.aspose.words/tabstopcollection/).

 **Examples:** 

Показывает, как изменить позицию правой табуляции в абзацах, связанных с оглавлением (TOC).

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [TabStop(double position)](#TabStop-double) | Инициализирует новый экземпляр этого класса. |
| [TabStop(double position, int alignment, int leader)](#TabStop-double-int-int) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(TabStop rhs)](#equals-com.aspose.words.TabStop) | Сравнивает с указанным [TabStop](../../com.aspose.words/tabstop/). |
| [getAlignment()](#getAlignment) | Получает выравнивание текста в этой табуляции. |
| [getLeader()](#getLeader) | Получает тип линии‑заполнителя, отображаемой под символом табуляции. |
| [getPosition()](#getPosition) | Получает позицию табуляции в пунктах. |
| [hashCode()](#hashCode) |  |
| [isClear()](#isClear) | Возвращает  true  если эта табуляция очищает любые существующие табуляции в этой позиции. |
| [setAlignment(int value)](#setAlignment-int) | Устанавливает выравнивание текста в этой табуляции. |
| [setLeader(int value)](#setLeader-int) | Устанавливает тип линии‑заполнителя, отображаемой под символом табуляции. |
### TabStop(double position) {#TabStop-double}
```
public TabStop(double position)
```


Инициализирует новый экземпляр этого класса.

 **Examples:** 

Показывает, как работать с коллекцией табуляций документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| позиция | double |  |

### TabStop(double position, int alignment, int leader) {#TabStop-double-int-int}
```
public TabStop(double position, int alignment, int leader)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| позиция | double |  |
| выравнивание | int |  |
| заполнитель | int |  |

### equals(TabStop rhs) {#equals-com.aspose.words.TabStop}
```
public boolean equals(TabStop rhs)
```


Сравнивает с указанным [TabStop](../../com.aspose.words/tabstop/).

 **Examples:** 

Показывает, как работать с коллекцией табуляций документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| rhs | [TabStop](../../com.aspose.words/tabstop/) |  |

**Returns:**
boolean
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Получает выравнивание текста в этой табуляции.

 **Examples:** 

Показывает, как изменить позицию правой табуляции в абзацах, связанных с оглавлением (TOC).

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
int - Выравнивание текста в этой табуляции. Возвращаемое значение является одной из констант [TabAlignment](../../com.aspose.words/tabalignment/).
### getLeader() {#getLeader}
```
public int getLeader()
```


Получает тип линии‑заполнителя, отображаемой под символом табуляции.

 **Examples:** 

Показывает, как изменить позицию правой табуляции в абзацах, связанных с оглавлением (TOC).

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
int - Тип линии‑заполнителя, отображаемой под символом табуляции. Возвращаемое значение является одной из констант [TabLeader](../../com.aspose.words/tableader/).
### getPosition() {#getPosition}
```
public double getPosition()
```


Получает позицию табуляции в пунктах.

 **Examples:** 

Показывает, как изменить позицию правой табуляции в абзацах, связанных с оглавлением (TOC).

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
double - Позиция табуляции в пунктах.
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


Возвращает  true  если эта табуляция очищает любые существующие табуляции в этой позиции.

 **Examples:** 

Показывает, как работать с коллекцией табуляций документа.

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
boolean -  true  если эта табуляция удаляет любые существующие табуляции в этой позиции.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Устанавливает выравнивание текста в этой табуляции.

 **Examples:** 

Показывает, как изменить позицию правой табуляции в абзацах, связанных с оглавлением (TOC).

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Выравнивание текста в этой табуляции. Значение должно быть одной из констант [TabAlignment](../../com.aspose.words/tabalignment/). |

### setLeader(int value) {#setLeader-int}
```
public void setLeader(int value)
```


Устанавливает тип линии‑заполнителя, отображаемой под символом табуляции.

 **Examples:** 

Показывает, как изменить позицию правой табуляции в абзацах, связанных с оглавлением (TOC).

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Тип линии‑заполнителя, отображаемой под символом табуляции. Значение должно быть одной из констант [TabLeader](../../com.aspose.words/tableader/). |

