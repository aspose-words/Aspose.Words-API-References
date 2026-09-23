---
title: "ListCollection"
linktitle: "ListCollection"
second_title: "Aspose.Words pour Java"
description: "Stocke et gère le formatage des listes à puces et numérotées utilisées dans un document en Java."
type: docs
weight: 426
url: /fr/java/com.aspose.words/listcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListCollection implements Cloneable, Iterable
```

Stocke et gère le formatage des listes à puces et numérotées utilisées dans un document.

Pour en savoir plus, consultez l'article de documentation [ Working with Lists ][Working with Lists].

 **Remarks:** 

Une liste dans un document Microsoft Word est un ensemble de propriétés de formatage de liste. Le formatage des listes est stocké dans la collection [ListCollection](../../com.aspose.words/listcollection/) séparément des paragraphes de texte.

Vous ne créez pas d'objets de cette classe. Il n'existe toujours qu'un seul objet [ListCollection](../../com.aspose.words/listcollection/) par document et il est accessible via la propriété [DocumentBase.getLists()](../../com.aspose.words/documentbase/\#getLists).

Pour créer une nouvelle liste basée sur un modèle de liste prédéfini ou sur un style de liste, utilisez la méthode [add(com.aspose.words.Style)](../../com.aspose.words/listcollection/\#add-com.aspose.words.Style).

Pour créer une nouvelle liste avec un format identique à une liste existante, utilisez la méthode [addCopy(com.aspose.words.List)](../../com.aspose.words/listcollection/\#addCopy-com.aspose.words.List).

Pour rendre un paragraphe à puces ou numéroté, vous devez appliquer le format de liste à un paragraphe en attribuant un objet [List](../../com.aspose.words/list/) à la propriété [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) de [ListFormat](../../com.aspose.words/listformat/).

Pour supprimer le format de liste d'un paragraphe, utilisez la méthode [ListFormat.removeNumbers()](../../com.aspose.words/listformat/\#removeNumbers).

Si vous connaissez un peu le WordprocessingML, vous savez peut‑être qu’il définit des concepts séparés pour « list » et « list definition ». Cela correspond exactement à la façon dont le format de liste est stocké dans un document Microsoft Word au niveau bas. La définition de liste est comme un « schéma » et la liste est comme une instance d’une définition de liste.

Pour simplifier le modèle de programmation, Aspose.Words masque la distinction entre liste et définition de liste de la même manière que Microsoft Word la masque dans son interface utilisateur. Cela vous permet de vous concentrer davantage sur l’apparence souhaitée de votre document, plutôt que de créer des objets de bas niveau pour satisfaire les exigences du format de fichier Microsoft Word.

Il n’est pas possible de supprimer les listes une fois créées dans la version actuelle d’Aspose.Words. C’est similaire à Microsoft Word où l’utilisateur n’a pas de contrôle explicite sur les définitions de listes.

 **Examples:** 

Montre comment travailler avec les niveaux de liste.

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

Montre comment redémarrer la numérotation dans une liste en copiant une liste.

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

Montre comment créer un document avec un exemple de toutes les listes d’un autre document.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(Style listStyle)](#add-com.aspose.words.Style) | Crée une nouvelle liste qui référence un style de liste et l’ajoute à la collection de listes du document. |
| [add(int listTemplate)](#add-int) |  |
| [addCopy(List srcList)](#addCopy-com.aspose.words.List) | Crée une nouvelle liste en copiant la liste spécifiée et en l’ajoutant à la collection de listes du document. |
| [addSingleLevelList(int listTemplate)](#addSingleLevelList-int) |  |
| [get(int index)](#get-int) | Obtient une liste par indice. |
| [getCount()](#getCount) | Obtient le nombre de listes numérotées et à puces dans le document. |
| [getDocument()](#getDocument) | Obtient le document propriétaire. |
| [getListByListId(int listId)](#getListByListId-int) | Obtient une liste par un identifiant de liste. |
| [iterator()](#iterator) | Obtient l’objet énumérateur qui parcourra les listes du document. |
### add(Style listStyle) {#add-com.aspose.words.Style}
```
public List add(Style listStyle)
```


Crée une nouvelle liste qui référence un style de liste et l’ajoute à la collection de listes du document.

 **Remarks:** 

La nouvelle liste créée référence le style de liste. Si vous modifiez les propriétés du style de liste, elles sont reflétées dans les propriétés de la liste. Inversement, si vous modifiez les propriétés de la liste, elles sont reflétées dans les propriétés du style de liste.

 **Examples:** 

Montre comment créer un style de liste et l’utiliser dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| listStyle | [Style](../../com.aspose.words/style/) | Le style de liste. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### add(int listTemplate) {#add-int}
```
public List add(int listTemplate)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### addCopy(List srcList) {#addCopy-com.aspose.words.List}
```
public List addCopy(List srcList)
```


Crée une nouvelle liste en copiant la liste spécifiée et en l’ajoutant à la collection de listes du document.

 **Remarks:** 

La liste source peut provenir de n’importe quel document. Si la liste source appartient à un document différent, une copie de la liste est créée et ajoutée au document actuel.

Si la liste source est une référence ou une définition d’un style de liste, la nouvelle liste créée n’est pas liée au style de liste original.

 **Examples:** 

Montre comment redémarrer la numérotation dans une liste en copiant une liste.

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

Montre comment créer un document avec un exemple de toutes les listes d’un autre document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| srcList | [List](../../com.aspose.words/list/) | La liste source à copier. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### addSingleLevelList(int listTemplate) {#addSingleLevelList-int}
```
public List addSingleLevelList(int listTemplate)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### get(int index) {#get-int}
```
public List get(int index)
```


Obtient une liste par indice.

 **Examples:** 

Montre comment appliquer le format de liste d’une liste existante à une collection de paragraphes.

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

Montre comment vérifier les propriétés du document propriétaire des listes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[List](../../com.aspose.words/list/) - A list by index.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre de listes numérotées et à puces dans le document.

 **Examples:** 

Montre comment vérifier les propriétés du document propriétaire des listes.

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
int - Le nombre de listes numérotées et à puces dans le document.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Obtient le document propriétaire.

 **Examples:** 

Montre comment vérifier les propriétés du document propriétaire des listes.

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


Obtient une liste par un identifiant de liste.

 **Remarks:** 

Vous n’avez généralement pas besoin d’utiliser cette méthode. La plupart du temps, vous appliquez le format de liste aux paragraphes simplement en réglant la propriété [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) de l’objet [ListFormat](../../com.aspose.words/listformat/).

 **Examples:** 

Montre comment vérifier les propriétés du document propriétaire des listes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| listId | int | L'identifiant de la liste. |

**Returns:**
[List](../../com.aspose.words/list/) - Returns the list object. Returns  null  if a list with the specified identifier was not found.
### iterator() {#iterator}
```
public Iterator iterator()
```


Obtient l’objet énumérateur qui parcourra les listes du document.

 **Examples:** 

Montre comment créer un document avec un exemple de toutes les listes d’un autre document.

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
