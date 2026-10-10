---
title: "ListCollection"
linktitle: "ListCollection"
second_title: "Aspose.Words für Java"
description: "Speichert und verwaltet die Formatierung von Aufzählungs- und nummerierten Listen, die in einem Dokument in Java verwendet werden."
type: docs
weight: 426
url: /de/java/com.aspose.words/listcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListCollection implements Cloneable, Iterable
```

Speichert und verwaltet die Formatierung von Aufzählungs‑ und nummerierten Listen, die in einem Dokument verwendet werden.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Lists ][Working with Lists].

 **Remarks:** 

Eine Liste in einem Microsoft Word-Dokument ist ein Satz von Listformatierungseigenschaften. Die Formatierung der Listen wird in der [ListCollection](../../com.aspose.words/listcollection/) Sammlung getrennt von den Textabsätzen gespeichert.

Sie erstellen keine Objekte dieser Klasse. Pro Dokument gibt es immer nur ein [ListCollection](../../com.aspose.words/listcollection/) Objekt, das über die Eigenschaft [DocumentBase.getLists()](../../com.aspose.words/documentbase/\#getLists) zugänglich ist.

Um eine neue Liste basierend auf einer vordefinierten Listenvorlage oder einem Liststil zu erstellen, verwenden Sie die Methode [add(com.aspose.words.Style)](../../com.aspose.words/listcollection/\#add-com.aspose.words.Style).

Um eine neue Liste mit einer Formatierung zu erstellen, die einer bestehenden Liste identisch ist, verwenden Sie die Methode [addCopy(com.aspose.words.List)](../../com.aspose.words/listcollection/\#addCopy-com.aspose.words.List).

Um einen Absatz mit Aufzählungszeichen oder Nummerierung zu versehen, müssen Sie die Listformatierung auf einen Absatz anwenden, indem Sie ein [List](../../com.aspose.words/list/) Objekt der Eigenschaft [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) von [ListFormat](../../com.aspose.words/listformat/) zuweisen.

Um die Listformatierung von einem Absatz zu entfernen, verwenden Sie die Methode [ListFormat.removeNumbers()](../../com.aspose.words/listformat/\#removeNumbers).

Wenn Sie ein wenig über WordprocessingML wissen, dann wissen Sie vielleicht, dass es separate Konzepte für \"list\" und \"list definition\" definiert. Das entspricht genau der Art und Weise, wie Listformatierung auf niedriger Ebene in einem Microsoft‑Word‑Dokument gespeichert wird. Eine Listendefinition ist wie ein \"Schema\" und eine Liste ist wie eine Instanz einer Listendefinition.

Um das Programmiermodell zu vereinfachen, verbirgt Aspose.Words die Unterscheidung zwischen Liste und Listendefinition in ähnlicher Weise, wie Microsoft Word dies in seiner Benutzeroberfläche verbirgt. Dadurch können Sie sich mehr darauf konzentrieren, wie Ihr Dokument aussehen soll, anstatt Low‑Level‑Objekte zu erstellen, um die Anforderungen des Microsoft‑Word‑Dateiformats zu erfüllen.

In der aktuellen Version von Aspose.Words ist es nicht möglich, Listen zu löschen, sobald sie erstellt wurden. Das ist ähnlich wie bei Microsoft Word, wo der Benutzer keine explizite Kontrolle über Listendefinitionen hat.

 **Examples:** 

Zeigt, wie man mit Listenebenen arbeitet.

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

Zeigt, wie man die Nummerierung in einer Liste durch Kopieren einer Liste neu startet.

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

Zeigt, wie man ein Dokument mit einem Beispiel aller Listen aus einem anderen Dokument erstellt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(Style listStyle)](#add-com.aspose.words.Style) | Erstellt eine neue Liste, die auf einen Liststil verweist, und fügt sie der Listensammlung im Dokument hinzu. |
| [add(int listTemplate)](#add-int) |  |
| [addCopy(List srcList)](#addCopy-com.aspose.words.List) | Erstellt eine neue Liste, indem die angegebene Liste kopiert wird, und fügt sie der Listensammlung im Dokument hinzu. |
| [addSingleLevelList(int listTemplate)](#addSingleLevelList-int) |  |
| [get(int index)](#get-int) | Ruft eine Liste nach Index ab. |
| [getCount()](#getCount) | Ermittelt die Anzahl nummerierter und Aufzählungslisten im Dokument. |
| [getDocument()](#getDocument) | Ruft das zugehörige Dokument ab. |
| [getListByListId(int listId)](#getListByListId-int) | Ruft eine Liste anhand einer Listenkennung ab. |
| [iterator()](#iterator) | Ruft das Enumerator‑Objekt ab, das die Listen im Dokument aufzählt. |
### add(Style listStyle) {#add-com.aspose.words.Style}
```
public List add(Style listStyle)
```


Erstellt eine neue Liste, die auf einen Liststil verweist, und fügt sie der Listensammlung im Dokument hinzu.

 **Remarks:** 

Die neu erstellte Liste verweist auf den Liststil. Wenn Sie die Eigenschaften des Liststils ändern, werden sie in den Eigenschaften der Liste widergespiegelt. Umgekehrt, wenn Sie die Eigenschaften der Liste ändern, werden sie in den Eigenschaften des Liststils widergespiegelt.

 **Examples:** 

Zeigt, wie man einen Liststil erstellt und in einem Dokument verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listStyle | [Style](../../com.aspose.words/style/) | Der Liststil. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### add(int listTemplate) {#add-int}
```
public List add(int listTemplate)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### addCopy(List srcList) {#addCopy-com.aspose.words.List}
```
public List addCopy(List srcList)
```


Erstellt eine neue Liste, indem die angegebene Liste kopiert wird, und fügt sie der Listensammlung im Dokument hinzu.

 **Remarks:** 

Die Quellliste kann aus jedem Dokument stammen. Wenn die Quellliste zu einem anderen Dokument gehört, wird eine Kopie der Liste erstellt und dem aktuellen Dokument hinzugefügt.

Wenn die Quellliste eine Referenz auf oder eine Definition eines Liststils ist, steht die neu erstellte Liste nicht in Beziehung zum ursprünglichen Liststil.

 **Examples:** 

Zeigt, wie man die Nummerierung in einer Liste durch Kopieren einer Liste neu startet.

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

Zeigt, wie man ein Dokument mit einem Beispiel aller Listen aus einem anderen Dokument erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcList | [List](../../com.aspose.words/list/) | Die Quellliste, von der kopiert werden soll. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### addSingleLevelList(int listTemplate) {#addSingleLevelList-int}
```
public List addSingleLevelList(int listTemplate)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### get(int index) {#get-int}
```
public List get(int index)
```


Ruft eine Liste nach Index ab.

 **Examples:** 

Zeigt, wie man die Listformatierung einer vorhandenen Liste auf eine Sammlung von Absätzen anwendet.

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

Zeigt, wie man die Eigenschaften des zugehörigen Dokuments von Listen überprüft.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
[List](../../com.aspose.words/list/) - A list by index.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl nummerierter und Aufzählungslisten im Dokument.

 **Examples:** 

Zeigt, wie man die Eigenschaften des zugehörigen Dokuments von Listen überprüft.

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
int – Die Anzahl nummerierter und Aufzählungslisten im Dokument.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Ruft das zugehörige Dokument ab.

 **Examples:** 

Zeigt, wie man die Eigenschaften des zugehörigen Dokuments von Listen überprüft.

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


Ruft eine Liste anhand einer Listenkennung ab.

 **Remarks:** 

Sie müssen diese Methode normalerweise nicht verwenden. Meistens wenden Sie die Listformatierung auf Absätze an, indem Sie einfach die [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) Eigenschaft des [ListFormat](../../com.aspose.words/listformat/) Objekts.

 **Examples:** 

Zeigt, wie man die Eigenschaften des zugehörigen Dokuments von Listen überprüft.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listId | int | Der Listenbezeichner. |

**Returns:**
[List](../../com.aspose.words/list/) - Returns the list object. Returns  null  if a list with the specified identifier was not found.
### iterator() {#iterator}
```
public Iterator iterator()
```


Ruft das Enumerator‑Objekt ab, das die Listen im Dokument aufzählt.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem Beispiel aller Listen aus einem anderen Dokument erstellt.

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
