---
title: "TabStopCollection"
linktitle: "TabStopCollection"
second_title: "Aspose.Words لـ Java"
description: "مجموعة من كائنات TabStop التي تمثل علامات تبويب مخصصة لفقرة أو نمط في Java."
type: docs
weight: 655
url: /ar/java/com.aspose.words/tabstopcollection/
---

**Inheritance:**
java.lang.Object، [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStopCollection extends InternableComplexAttr implements Cloneable
```

مجموعة من كائنات [TabStop](../../com.aspose.words/tabstop/) التي تمثل علامات تبويب مخصصة لفقرة أو نمط.

لمزيد من المعلومات، قم بزيارة مقالة وثائق [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_]

 **Remarks:** 

في مستندات Microsoft Word، يمكن تعريف علامة تبويب في خصائص نمط الفقرة أو مباشرةً في خصائص الفقرة. يمكن أن يكون النمط مستندًا إلى نمط آخر. لذلك، فإن مجموعة علامات التبويب الكاملة لكائن معين هي مزيج من علامات التبويب المعرفة مباشرةً على هذا الكائن وعلامات التبويب الموروثة من الأنماط الأصلية.

في Aspose.Words، عندما تحصل على [TabStopCollection](../../com.aspose.words/tabstopcollection/) لفقرة أو نمط، فإنه يحتوي فقط على علامات التبويب المخصصة المعرفة مباشرةً لهذه الفقرة أو النمط. لا تشمل المجموعة علامات التبويب المعرفة في الأنماط الأصلية أو علامات التبويب الافتراضية.

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


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(TabStop tabStop)](#add-com.aspose.words.TabStop) | يضيف أو يستبدل علامة تبويب في المجموعة. |
| [add(double position, int alignment, int leader)](#add-double-int-int) |  |
| [after(double position)](#after-double) | يحصل على أول علامة تبويب إلى يمين الموضع المحدد. |
| [before(double position)](#before-double) | يحصل على أول علامة تبويب إلى يسار الموضع المحدد. |
| [clear()](#clear) | يحذف جميع مواضع علامات التبويب. |
| [equals(TabStopCollection rhs)](#equals-com.aspose.words.TabStopCollection) | يحدد ما إذا كانت مجموعة [TabStopCollection](../../com.aspose.words/tabstopcollection/) المحددة مساوية في القيمة إلى مجموعة [TabStopCollection](../../com.aspose.words/tabstopcollection/) الحالية. |
| [equals(Object obj)](#equals-java.lang.Object) | يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي. |
| [get(double position)](#get-double) | يحصل على علامة تبويب عند الموضع المحدد. |
| [get(int index)](#get-int) | يسترجع علامة تبويب من المجموعة. |
| [getCount()](#getCount) | يحصل على عدد علامات التبويب في المجموعة. |
| [getIndexByPosition(double position)](#getIndexByPosition-double) | يحصل على فهرس علامة تبويب بالموضع المحدد بالنقاط. |
| [getPositionByIndex(int index)](#getPositionByIndex-int) | يحصل على الموضع (بالنقاط) لعلامة التبويب عند الفهرس المحدد. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [removeByIndex(int index)](#removeByIndex-int) | يزيل علامة تبويب عند الفهرس المحدد من المجموعة. |
| [removeByPosition(double position)](#removeByPosition-double) | يزيل علامة تبويب عند الموضع المحدد من المجموعة. |
### add(TabStop tabStop) {#add-com.aspose.words.TabStop}
```
public void add(TabStop tabStop)
```


يضيف أو يستبدل علامة تبويب في المجموعة.

 **Remarks:** 

إذا كانت علامة تبويب موجودة بالفعل عند الموضع المحدد، يتم استبدالها.

 **Examples:** 

يظهر كيفية إضافة علامات تبويب مخصصة إلى مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| tabStop | [TabStop](../../com.aspose.words/tabstop/) | كائن علامة تبويب للإضافة. |

### add(double position, int alignment, int leader) {#add-double-int-int}
```
public void add(double position, int alignment, int leader)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الموضع | double |  |
| المحاذاة | int |  |
| المحدد | int |  |

### after(double position) {#after-double}
```
public TabStop after(double position)
```


يحصل على أول علامة تبويب إلى يمين الموضع المحدد.

 **Remarks:** 

يتخطى علامات التبويب التي تم تعيين [TabStop.getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) لها إلى [TabAlignment.BAR](../../com.aspose.words/tabalignment/\#BAR).

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
| الموضع | double | موضع الإشارة (بالنقاط). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop object or  null  if a suitable tab stop was not found.
### before(double position) {#before-double}
```
public TabStop before(double position)
```


يحصل على أول علامة تبويب إلى يسار الموضع المحدد.

 **Remarks:** 

يتخطى علامات التبويب التي تم تعيين [TabStop.getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) لها إلى [TabAlignment.BAR](../../com.aspose.words/tabalignment/\#BAR).

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
| الموضع | double | موضع الإشارة (بالنقاط). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop object or  null  if a suitable tab stop was not found.
### clear() {#clear}
```
public void clear()
```


يحذف جميع مواضع علامات التبويب.

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

### equals(TabStopCollection rhs) {#equals-com.aspose.words.TabStopCollection}
```
public boolean equals(TabStopCollection rhs)
```


يحدد ما إذا كانت مجموعة [TabStopCollection](../../com.aspose.words/tabstopcollection/) المحددة مساوية في القيمة إلى مجموعة [TabStopCollection](../../com.aspose.words/tabstopcollection/) الحالية.

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
| rhs | [TabStopCollection](../../com.aspose.words/tabstopcollection/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي.

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
| obj | java.lang.Object |  |

**Returns:**
boolean
### get(double position) {#get-double}
```
public TabStop get(double position)
```


يحصل على علامة تبويب عند الموضع المحدد.

 **Remarks:** 

يرجع  null  إذا لم يتم العثور على علامة تبويب عند الموضع المحدد.

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
| الموضع | double | الموضع (بالنقاط) لعلامة التبويب. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop at the specified position.
### get(int index) {#get-int}
```
public TabStop get(int index)
```


يسترجع علامة تبويب من المجموعة.  يحصل على علامة تبويب عند الفهرس المعطى.

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
| الفهرس | int | فهرس في مجموعة علامات التبويب. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - The corresponding [TabStop](../../com.aspose.words/tabstop/) value.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد علامات التبويب في المجموعة.

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
int - عدد علامات التبويب في المجموعة.
### getIndexByPosition(double position) {#getIndexByPosition-double}
```
public int getIndexByPosition(double position)
```


يحصل على فهرس علامة تبويب بالموضع المحدد بالنقاط.

 **Examples:** 

يظهر كيفية البحث عن موضع لمعرفة ما إذا كانت علامة تبويب موجودة هناك والحصول على فهرسها.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الموضع | double |  |

**Returns:**
int
### getPositionByIndex(int index) {#getPositionByIndex-int}
```
public double getPositionByIndex(int index)
```


يحصل على الموضع (بالنقاط) لعلامة التبويب عند الفهرس المحدد.

 **Examples:** 

يظهر كيفية العثور على علامة تبويب بواسطة فهرسها والتحقق من موضعها.

```

 Document doc = new Document();
 TabStopCollection tabStops = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getTabStops();

 tabStops.add(ConvertUtil.millimeterToPoint(30.0), TabAlignment.LEFT, TabLeader.DASHES);
 tabStops.add(ConvertUtil.millimeterToPoint(60.0), TabAlignment.LEFT, TabLeader.DASHES);

 // Verify the position of the second tab stop in the collection.
 Assert.assertEquals(ConvertUtil.millimeterToPoint(60.0), tabStops.getPositionByIndex(1), 0.1d);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس في مجموعة علامات التبويب. |

**Returns:**
double - موضع علامة التبويب.
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


يزيل علامة تبويب عند الفهرس المحدد من المجموعة.

 **Examples:** 

يظهر كيفية اختيار علامة تبويب في مستند بواسطة فهرسها وإزالتها.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس في مجموعة علامات التبويب. |

### removeByPosition(double position) {#removeByPosition-double}
```
public void removeByPosition(double position)
```


يزيل علامة تبويب عند الموضع المحدد من المجموعة.

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
| الموضع | double | الموضع (بالنقاط) لعلامة التبويب التي سيتم إزالتها. |

