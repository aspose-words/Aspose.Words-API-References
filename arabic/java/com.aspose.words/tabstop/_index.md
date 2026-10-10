---
title: "TabStop"
linktitle: "TabStop"
second_title: "Aspose.Words لـ Java"
description: "يمثل موضع تبويب مخصص واحد في Java."
type: docs
weight: 654
url: /ar/java/com.aspose.words/tabstop/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStop implements Cloneable
```

يمثل موضع تبويب مخصص واحد. الكائن [TabStop](../../com.aspose.words/tabstop/) هو عضو في مجموعة [TabStopCollection](../../com.aspose.words/tabstopcollection/).

لمزيد من المعلومات، قم بزيارة مقالة وثائق [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_]

 **Remarks:** 

عادةً، يحدد موضع التبويب موقعًا يوجد فيه موضع تبويب. ولكن نظرًا لأنه يمكن وراثة مواضع التبويب من الأنماط الأصلية، قد يكون من الضروري للعنصر الفرعي أن يحدد صراحةً عدم وجود موضع تبويب في موقع معين. لمسح موضع تبويب موروث في موقع معين، أنشئ كائنًا [TabStop](../../com.aspose.words/tabstop/) واضبط [getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) إلى [TabAlignment.CLEAR](../../com.aspose.words/tabalignment/\#CLEAR).

لمزيد من المعلومات راجع [TabStopCollection](../../com.aspose.words/tabstopcollection/).

 **Examples:** 

يعرض كيفية تعديل موضع علامة التبويب اليمنى في الفقرات المتعلقة بالفهرس.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [TabStop(double position)](#TabStop-double) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [TabStop(double position, int alignment, int leader)](#TabStop-double-int-int) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [equals(TabStop rhs)](#equals-com.aspose.words.TabStop) | يقارن مع [TabStop](../../com.aspose.words/tabstop/) المحدد. |
| [getAlignment()](#getAlignment) | يحصل على محاذاة النص عند هذا موضع التبويب. |
| [getLeader()](#getLeader) | يحصل على نوع الخط القائد المعروض تحت حرف التبويب. |
| [getPosition()](#getPosition) | يحصل على موقع موضع التبويب بالنقاط. |
| [hashCode()](#hashCode) |  |
| [isClear()](#isClear) | يرجع  true  إذا كان هذا موضع التبويب يمسح أي مواضد تبويب موجودة في هذا الموقع. |
| [setAlignment(int value)](#setAlignment-int) | يضبط محاذاة النص عند هذا موضع التبويب. |
| [setLeader(int value)](#setLeader-int) | يضبط نوع الخط القائد المعروض تحت حرف التبويب. |
### TabStop(double position) {#TabStop-double}
```
public TabStop(double position)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

 **Examples:** 

يظهر كيفية العمل مع مجموعة علامات التبويب في المستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الموضع | double |  |

### TabStop(double position, int alignment, int leader) {#TabStop-double-int-int}
```
public TabStop(double position, int alignment, int leader)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الموضع | double |  |
| المحاذاة | int |  |
| المحدد | int |  |

### equals(TabStop rhs) {#equals-com.aspose.words.TabStop}
```
public boolean equals(TabStop rhs)
```


يقارن مع [TabStop](../../com.aspose.words/tabstop/) المحدد.

 **Examples:** 

يظهر كيفية العمل مع مجموعة علامات التبويب في المستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| rhs | [TabStop](../../com.aspose.words/tabstop/) |  |

**Returns:**
boolean
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


يحصل على محاذاة النص عند هذا موضع التبويب.

 **Examples:** 

يعرض كيفية تعديل موضع علامة التبويب اليمنى في الفقرات المتعلقة بالفهرس.

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
int - محاذاة النص عند هذه النقطة التبويبية. القيمة المرجعة هي واحدة من ثوابت [TabAlignment](../../com.aspose.words/tabalignment/).
### getLeader() {#getLeader}
```
public int getLeader()
```


يحصل على نوع الخط القائد المعروض تحت حرف التبويب.

 **Examples:** 

يعرض كيفية تعديل موضع علامة التبويب اليمنى في الفقرات المتعلقة بالفهرس.

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
int - نوع خط القائد المعروض تحت حرف التبويب. القيمة المرجعة هي واحدة من ثوابت [TabLeader](../../com.aspose.words/tableader/).
### getPosition() {#getPosition}
```
public double getPosition()
```


يحصل على موقع موضع التبويب بالنقاط.

 **Examples:** 

يعرض كيفية تعديل موضع علامة التبويب اليمنى في الفقرات المتعلقة بالفهرس.

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
double - موضع نقطة التبويب بالنقاط.
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


يرجع  true  إذا كان هذا موضع التبويب يمسح أي مواضد تبويب موجودة في هذا الموقع.

 **Examples:** 

يظهر كيفية العمل مع مجموعة علامات التبويب في المستند.

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
boolean -  true  إذا كانت هذه النقطة التبويبية تمسح أي نقاط تبويب موجودة في هذا الموضع.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


يضبط محاذاة النص عند هذا موضع التبويب.

 **Examples:** 

يعرض كيفية تعديل موضع علامة التبويب اليمنى في الفقرات المتعلقة بالفهرس.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | محاذاة النص عند هذه النقطة التبويبية. يجب أن تكون القيمة واحدة من ثوابت [TabAlignment](../../com.aspose.words/tabalignment/). |

### setLeader(int value) {#setLeader-int}
```
public void setLeader(int value)
```


يضبط نوع الخط القائد المعروض تحت حرف التبويب.

 **Examples:** 

يعرض كيفية تعديل موضع علامة التبويب اليمنى في الفقرات المتعلقة بالفهرس.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | نوع خط القائد المعروض تحت حرف التبويب. يجب أن تكون القيمة واحدة من ثوابت [TabLeader](../../com.aspose.words/tableader/). |

