---
title: "ListCollection"
linktitle: "ListCollection"
second_title: "Aspose.Words لـ Java"
description: "يخزن ويدير تنسيق القوائم النقطية والمرقمة المستخدمة في مستند بلغة Java."
type: docs
weight: 426
url: /ar/java/com.aspose.words/listcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListCollection implements Cloneable, Iterable
```

يخزن ويدير تنسيق القوائم النقطية والمرقمة المستخدمة في المستند.

لمعرفة المزيد، زر مقالة الوثائق [ Working with Lists ][Working with Lists].

 **Remarks:** 

القائمة في مستند Microsoft Word هي مجموعة من خصائص تنسيق القوائم. يتم تخزين تنسيق القوائم في مجموعة [ListCollection](../../com.aspose.words/listcollection/) بشكل منفصل عن فقرات النص.

أنت لا تنشئ كائنات من هذه الفئة. يوجد دائمًا كائن واحد فقط من نوع [ListCollection](../../com.aspose.words/listcollection/) لكل مستند ويمكن الوصول إليه عبر الخاصية [DocumentBase.getLists()](../../com.aspose.words/documentbase/#getLists).

لإنشاء قائمة جديدة بناءً على قالب قائمة مسبق التعريف أو بناءً على نمط قائمة، استخدم الطريقة [add(com.aspose.words.Style)](../../com.aspose.words/listcollection/#add-com.aspose.words.Style).

لإنشاء قائمة جديدة بتنسيق مطابق لقائمة موجودة، استخدم طريقة [addCopy(com.aspose.words.List)](../../com.aspose.words/listcollection/\#addCopy-com.aspose.words.List).

لجعل فقرة ذات تعداد نقطي أو رقمي، تحتاج إلى تطبيق تنسيق القائمة على الفقرة عن طريق تعيين كائن [List](../../com.aspose.words/list/) إلى الخاصية [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) في [ListFormat](../../com.aspose.words/listformat/).

لإزالة تنسيق القائمة من فقرة، استخدم طريقة [ListFormat.removeNumbers()](../../com.aspose.words/listformat/\#removeNumbers).

إذا كنت تعرف القليل عن WordprocessingML، فقد تعلم أنه يعرّف مفاهيم منفصلة لـ "list" و "list definition". وهذا يتطابق تمامًا مع الطريقة التي يتم بها تخزين تنسيق القائمة في مستند Microsoft Word على المستوى المنخفض. تعريف القائمة يشبه "المخطط" والقائمة تشبه نسخة من تعريف القائمة.

لتبسيط نموذج البرمجة، تقوم Aspose.Words بإخفاء التمييز بين القائمة وتعريف القائمة بنفس الطريقة التي يخفي بها Microsoft Word ذلك في واجهة المستخدم. هذا يسمح لك بالتركيز أكثر على الشكل الذي تريد أن يبدو عليه المستند، بدلاً من بناء كائنات منخفضة المستوى لتلبية متطلبات تنسيق ملف Microsoft Word.

ليس من الممكن حذف القوائم بمجرد إنشائها في الإصدار الحالي من Aspose.Words. وهذا مشابه لـ Microsoft Word حيث لا يمتلك المستخدم سيطرة صريحة على تعريفات القوائم.

 **Examples:** 

يعرض كيفية العمل مع مستويات القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertFalse(builder.getListFormat().isListItem());

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Below are two types of lists that we can create using a document builder.
 // 1 -  A numbered list:
 // Numbered lists create a logical order for their paragraphs by numbering each item.
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.NUMBER_DEFAULT));

 Assert.assertTrue(builder.getListFormat().isListItem());

 // By setting the "ListLevelNumber" property, we can increase the list level
 // to begin a self-contained sub-list at the current list item.
 // The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
 // Deeper list levels use letters and lowercase Roman numerals.
 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // 2 -  A bulleted list:
 // This list will apply an indent and a bullet symbol ("\u2022") before each paragraph.
 // Deeper levels of this list will use different symbols, such as "\u25a0" and "\u25cb".
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));

 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
 builder.getListFormat().setList(null);

 Assert.assertFalse(builder.getListFormat().isListItem());

 doc.save(getArtifactsDir() + "Lists.SpecifyListLevel.docx");
 
```

يعرض كيفية إعادة بدء الترقيم في قائمة عن طريق نسخ القائمة.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize its first list level.
 List list1 = doc.getLists().add(ListTemplate.NUMBER_ARABIC_PARENTHESIS);
 list1.getListLevels().get(0).getFont().setColor(Color.RED);
 list1.getListLevels().get(0).setAlignment(ListLevelAlignment.RIGHT);

 // Apply our list to some paragraphs.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("List 1 starts below:");
 builder.getListFormat().setList(list1);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 // We can add a copy of an existing list to the document's list collection
 // to create a similar list without making changes to the original.
 List list2 = doc.getLists().addCopy(list1);
 list2.getListLevels().get(0).getFont().setColor(Color.BLUE);
 list2.getListLevels().get(0).setStartAt(10);

 // Apply the second list to new paragraphs.
 builder.writeln("List 2 starts below:");
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.RestartNumberingUsingListCopy.docx");
 
```

يوضح كيفية إنشاء مستند يحتوي على عينة من جميع القوائم من مستند آخر.

```

 public void printOutAllLists() throws Exception {
     Document srcDoc = new Document(getMyDir() + "Rendering.docx");

     Document dstDoc = new Document();
     DocumentBuilder builder = new DocumentBuilder(dstDoc);

     for (List srcList : srcDoc.getLists()) {
         List dstList = dstDoc.getLists().addCopy(srcList);
         addListSample(builder, dstList);
     }

     dstDoc.save(getArtifactsDir() + "Lists.PrintOutAllLists.docx");
 }

 private static void addListSample(final DocumentBuilder builder, final List docList) {
     builder.writeln("Sample formatting of list with ListId:" + docList.getListId());
     builder.getListFormat().setList(docList);
     for (int i = 0; i < docList.getListLevels().getCount(); i++) {
         builder.getListFormat().setListLevelNumber(i);
         builder.writeln("Level " + i);
     }
     builder.getListFormat().removeNumbers();
     builder.writeln();
 }
 
```


[Working with Lists]: https://docs.aspose.com/words/java/working-with-lists/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(Style listStyle)](#add-com.aspose.words.Style) | ينشئ قائمة جديدة تشير إلى نمط قائمة ويضيفها إلى مجموعة القوائم في المستند. |
| [add(int listTemplate)](#add-int) |  |
| [addCopy(List srcList)](#addCopy-com.aspose.words.List) | ينشئ قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند. |
| [addSingleLevelList(int listTemplate)](#addSingleLevelList-int) |  |
| [get(int index)](#get-int) | يحصل على قائمة حسب الفهرس. |
| [getCount()](#getCount) | يحصل على عدد القوائم المرقمة والنقطية في المستند. |
| [getDocument()](#getDocument) | يحصل على المستند المالك. |
| [getListByListId(int listId)](#getListByListId-int) | يحصل على قائمة حسب معرف القائمة. |
| [iterator()](#iterator) | يحصل على كائن المُعدِّد الذي سيعد القوائم في المستند. |
### add(Style listStyle) {#add-com.aspose.words.Style}
```
public List add(Style listStyle)
```


ينشئ قائمة جديدة تشير إلى نمط قائمة ويضيفها إلى مجموعة القوائم في المستند.

 **Remarks:** 

القائمة التي تم إنشاؤها حديثًا تشير إلى نمط القائمة. إذا قمت بتغيير خصائص نمط القائمة، فإن ذلك ينعكس في خصائص القائمة. والعكس صحيح، إذا غيرت خصائص القائمة، فإن ذلك ينعكس في خصائص نمط القائمة.

 **Examples:** 

يوضح كيفية إنشاء نمط قائمة واستخدامه في مستند.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // We can contain an entire List object within a style.
 Style listStyle = doc.getStyles().add(StyleType.LIST, "MyListStyle");

 List list1 = listStyle.getList();

 Assert.assertTrue(list1.isListStyleDefinition());
 Assert.assertFalse(list1.isListStyleReference());
 Assert.assertTrue(list1.isMultiLevel());
 Assert.assertEquals(listStyle, list1.getStyle());

 // Change the appearance of all list levels in our list.
 for (ListLevel level : list1.getListLevels()) {
     level.getFont().setName("Verdana");
     level.getFont().setColor(Color.BLUE);
     level.getFont().setBold(true);
 }

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Using list style first time:");

 // Create another list from a list within a style.
 List list2 = doc.getLists().add(listStyle);

 Assert.assertFalse(list2.isListStyleDefinition());
 Assert.assertTrue(list2.isListStyleReference());
 Assert.assertEquals(listStyle, list2.getStyle());

 // Add some list items that our list will format.
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.writeln("Using list style second time:");

 // Create and apply another list based on the list style.
 List list3 = doc.getLists().add(listStyle);
 builder.getListFormat().setList(list3);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateAndUseListStyle.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| listStyle | [Style](../../com.aspose.words/style/) | نمط القائمة. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### add(int listTemplate) {#add-int}
```
public List add(int listTemplate)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### addCopy(List srcList) {#addCopy-com.aspose.words.List}
```
public List addCopy(List srcList)
```


ينشئ قائمة جديدة عن طريق نسخ القائمة المحددة وإضافتها إلى مجموعة القوائم في المستند.

 **Remarks:** 

يمكن أن تكون القائمة المصدر من أي مستند. إذا كانت القائمة المصدر تنتمي إلى مستند مختلف، يتم إنشاء نسخة من القائمة وإضافتها إلى المستند الحالي.

إذا كانت القائمة المصدر إشارة إلى أو تعريف لنمط قائمة، فإن القائمة التي تم إنشاؤها حديثًا لا ترتبط بنمط القائمة الأصلي.

 **Examples:** 

يعرض كيفية إعادة بدء الترقيم في قائمة عن طريق نسخ القائمة.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize its first list level.
 List list1 = doc.getLists().add(ListTemplate.NUMBER_ARABIC_PARENTHESIS);
 list1.getListLevels().get(0).getFont().setColor(Color.RED);
 list1.getListLevels().get(0).setAlignment(ListLevelAlignment.RIGHT);

 // Apply our list to some paragraphs.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("List 1 starts below:");
 builder.getListFormat().setList(list1);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 // We can add a copy of an existing list to the document's list collection
 // to create a similar list without making changes to the original.
 List list2 = doc.getLists().addCopy(list1);
 list2.getListLevels().get(0).getFont().setColor(Color.BLUE);
 list2.getListLevels().get(0).setStartAt(10);

 // Apply the second list to new paragraphs.
 builder.writeln("List 2 starts below:");
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.RestartNumberingUsingListCopy.docx");
 
```

يوضح كيفية إنشاء مستند يحتوي على عينة من جميع القوائم من مستند آخر.

```

 public void printOutAllLists() throws Exception {
     Document srcDoc = new Document(getMyDir() + "Rendering.docx");

     Document dstDoc = new Document();
     DocumentBuilder builder = new DocumentBuilder(dstDoc);

     for (List srcList : srcDoc.getLists()) {
         List dstList = dstDoc.getLists().addCopy(srcList);
         addListSample(builder, dstList);
     }

     dstDoc.save(getArtifactsDir() + "Lists.PrintOutAllLists.docx");
 }

 private static void addListSample(final DocumentBuilder builder, final List docList) {
     builder.writeln("Sample formatting of list with ListId:" + docList.getListId());
     builder.getListFormat().setList(docList);
     for (int i = 0; i < docList.getListLevels().getCount(); i++) {
         builder.getListFormat().setListLevelNumber(i);
         builder.writeln("Level " + i);
     }
     builder.getListFormat().removeNumbers();
     builder.writeln();
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| srcList | [List](../../com.aspose.words/list/) | القائمة المصدر للنسخ منها. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### addSingleLevelList(int listTemplate) {#addSingleLevelList-int}
```
public List addSingleLevelList(int listTemplate)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### get(int index) {#get-int}
```
public List get(int index)
```


يحصل على قائمة حسب الفهرس.

 **Examples:** 

يوضح كيفية تطبيق تنسيق القائمة لقائمة موجودة على مجموعة من الفقرات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1");
 builder.writeln("Paragraph 2");
 builder.write("Paragraph 3");

 NodeCollection paras = doc.getChildNodes(NodeType.PARAGRAPH, true);

 Assert.assertEquals(0, DocumentHelper.getListItemCount(paras));

 doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 List docList = doc.getLists().get(0);

 for (Paragraph paragraph : doc.getFirstSection().getBody().getParagraphs()) {
     paragraph.getListFormat().setList(docList);
     paragraph.getListFormat().setListLevelNumber(2);
 }

 paras = doc.getChildNodes(NodeType.PARAGRAPH, true);

 Assert.assertEquals(3, DocumentHelper.getListItemCount(paras));
 
```

يوضح كيفية التحقق من خصائص المستند المالك للقوائم.

```

 Document doc = new Document();

 ListCollection lists = doc.getLists();

 Assert.assertEquals(doc, lists.getDocument());

 List docList = lists.add(ListTemplate.BULLET_DEFAULT);
 Assert.assertEquals(doc, docList.getDocument());

 System.out.println("Current list count: " + lists.getCount());
 System.out.println("Is the first document list: " + (lists.get(0).equals(docList)));
 System.out.println("ListId: " + docList.getListId());
 System.out.println("List is the same by ListId: " + (lists.getListByListId(1).equals(docList)));
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
[List](../../com.aspose.words/list/) - A list by index.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد القوائم المرقمة والنقطية في المستند.

 **Examples:** 

يوضح كيفية التحقق من خصائص المستند المالك للقوائم.

```

 Document doc = new Document();

 ListCollection lists = doc.getLists();

 Assert.assertEquals(doc, lists.getDocument());

 List docList = lists.add(ListTemplate.BULLET_DEFAULT);
 Assert.assertEquals(doc, docList.getDocument());

 System.out.println("Current list count: " + lists.getCount());
 System.out.println("Is the first document list: " + (lists.get(0).equals(docList)));
 System.out.println("ListId: " + docList.getListId());
 System.out.println("List is the same by ListId: " + (lists.getListByListId(1).equals(docList)));
 
```

**Returns:**
int - عدد القوائم المرقمة والنقطية في المستند.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


يحصل على المستند المالك.

 **Examples:** 

يوضح كيفية التحقق من خصائص المستند المالك للقوائم.

```

 Document doc = new Document();

 ListCollection lists = doc.getLists();

 Assert.assertEquals(doc, lists.getDocument());

 List docList = lists.add(ListTemplate.BULLET_DEFAULT);
 Assert.assertEquals(doc, docList.getDocument());

 System.out.println("Current list count: " + lists.getCount());
 System.out.println("Is the first document list: " + (lists.get(0).equals(docList)));
 System.out.println("ListId: " + docList.getListId());
 System.out.println("List is the same by ListId: " + (lists.getListByListId(1).equals(docList)));
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### getListByListId(int listId) {#getListByListId-int}
```
public List getListByListId(int listId)
```


يحصل على قائمة حسب معرف القائمة.

 **Remarks:** 

عادةً لا تحتاج إلى استخدام هذه الطريقة. في معظم الأوقات تقوم بتطبيق تنسيق القائمة على الفقرات فقط عن طريق ضبط الخاصية [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) في كائن [ListFormat](../../com.aspose.words/listformat/).

 **Examples:** 

يوضح كيفية التحقق من خصائص المستند المالك للقوائم.

```

 Document doc = new Document();

 ListCollection lists = doc.getLists();

 Assert.assertEquals(doc, lists.getDocument());

 List docList = lists.add(ListTemplate.BULLET_DEFAULT);
 Assert.assertEquals(doc, docList.getDocument());

 System.out.println("Current list count: " + lists.getCount());
 System.out.println("Is the first document list: " + (lists.get(0).equals(docList)));
 System.out.println("ListId: " + docList.getListId());
 System.out.println("List is the same by ListId: " + (lists.getListByListId(1).equals(docList)));
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| listId | int | معرف القائمة. |

**Returns:**
[List](../../com.aspose.words/list/) - Returns the list object. Returns  null  if a list with the specified identifier was not found.
### iterator() {#iterator}
```
public Iterator iterator()
```


يحصل على كائن المُعدِّد الذي سيعد القوائم في المستند.

 **Examples:** 

يوضح كيفية إنشاء مستند يحتوي على عينة من جميع القوائم من مستند آخر.

```

 public void printOutAllLists() throws Exception {
     Document srcDoc = new Document(getMyDir() + "Rendering.docx");

     Document dstDoc = new Document();
     DocumentBuilder builder = new DocumentBuilder(dstDoc);

     for (List srcList : srcDoc.getLists()) {
         List dstList = dstDoc.getLists().addCopy(srcList);
         addListSample(builder, dstList);
     }

     dstDoc.save(getArtifactsDir() + "Lists.PrintOutAllLists.docx");
 }

 private static void addListSample(final DocumentBuilder builder, final List docList) {
     builder.writeln("Sample formatting of list with ListId:" + docList.getListId());
     builder.getListFormat().setList(docList);
     for (int i = 0; i < docList.getListLevels().getCount(); i++) {
         builder.getListFormat().setListLevelNumber(i);
         builder.writeln("Level " + i);
     }
     builder.getListFormat().removeNumbers();
     builder.writeln();
 }
 
```

**Returns:**
java.util.Iterator
