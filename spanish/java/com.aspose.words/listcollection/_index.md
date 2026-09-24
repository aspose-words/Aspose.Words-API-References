---
title: "ListCollection"
linktitle: "ListCollection"
second_title: "Aspose.Words para Java"
description: "Almacena y gestiona el formato de listas con viñetas y numeradas usadas en un documento en Java."
type: docs
weight: 426
url: /es/java/com.aspose.words/listcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListCollection implements Cloneable, Iterable
```

Almacena y gestiona el formato de listas con viñetas y numeradas utilizadas en un documento.

Para obtener más información, visite el artículo de documentación [ Working with Lists ][Working with Lists].

 **Remarks:** 

Una lista en un documento de Microsoft Word es un conjunto de propiedades de formato de lista. El formato de las listas se almacena en la colección [ListCollection](../../com.aspose.words/listcollection/) por separado de los párrafos de texto.

No crea objetos de esta clase. Siempre hay un solo objeto [ListCollection](../../com.aspose.words/listcollection/) por documento y es accesible a través de la propiedad [DocumentBase.getLists()](../../com.aspose.words/documentbase/\#getLists).

Para crear una nueva lista basada en una plantilla de lista predefinida o en un estilo de lista, use el método [add(com.aspose.words.Style)](../../com.aspose.words/listcollection/\#add-com.aspose.words.Style).

Para crear una nueva lista con un formato idéntico al de una lista existente, use el método [addCopy(com.aspose.words.List)](../../com.aspose.words/listcollection/\#addCopy-com.aspose.words.List).

Para que un párrafo tenga viñetas o numeración, necesita aplicar formato de lista a un párrafo asignando un objeto [List](../../com.aspose.words/list/) a la propiedad [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) de [ListFormat](../../com.aspose.words/listformat/).

Para eliminar el formato de lista de un párrafo, use el método [ListFormat.removeNumbers()](../../com.aspose.words/listformat/\#removeNumbers).

Si conoce un poco sobre WordprocessingML, entonces podría saber que define conceptos separados para "list" y "list definition". Esto corresponde exactamente a cómo se almacena el formato de lista en un documento de Microsoft Word a bajo nivel. La definición de lista es como un "esquema" y la lista es como una instancia de una definición de lista.

Para simplificar el modelo de programación, Aspose.Words oculta la distinción entre lista y definición de lista de manera similar a como Microsoft Word lo oculta en su interfaz de usuario. Esto le permite concentrarse más en cómo desea que se vea su documento, en lugar de construir objetos de bajo nivel para satisfacer los requisitos del formato de archivo de Microsoft Word.

No es posible eliminar listas una vez que se crean en la versión actual de Aspose.Words. Esto es similar a Microsoft Word, donde el usuario no tiene control explícito sobre las definiciones de lista.

 **Examples:** 

Muestra cómo trabajar con niveles de lista.

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

Muestra cómo reiniciar la numeración en una lista copiando una lista.

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

Muestra cómo crear un documento con una muestra de todas las listas de otro documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [add(Style listStyle)](#add-com.aspose.words.Style) | Crea una nueva lista que hace referencia a un estilo de lista y la agrega a la colección de listas del documento. |
| [add(int listTemplate)](#add-int) |  |
| [addCopy(List srcList)](#addCopy-com.aspose.words.List) | Crea una nueva lista copiando la lista especificada y agregándola a la colección de listas del documento. |
| [addSingleLevelList(int listTemplate)](#addSingleLevelList-int) |  |
| [get(int index)](#get-int) | Obtiene una lista por índice. |
| [getCount()](#getCount) | Obtiene el recuento de listas numeradas y con viñetas en el documento. |
| [getDocument()](#getDocument) | Obtiene el documento propietario. |
| [getListByListId(int listId)](#getListByListId-int) | Obtiene una lista mediante un identificador de lista. |
| [iterator()](#iterator) | Obtiene el objeto enumerador que enumerará las listas en el documento. |
### add(Style listStyle) {#add-com.aspose.words.Style}
```
public List add(Style listStyle)
```


Crea una nueva lista que hace referencia a un estilo de lista y la agrega a la colección de listas del documento.

 **Remarks:** 

La lista recién creada hace referencia al estilo de lista. Si cambia las propiedades del estilo de lista, se reflejan en las propiedades de la lista. Viceversa, si cambia las propiedades de la lista, se reflejan en las propiedades del estilo de lista.

 **Examples:** 

Muestra cómo crear un estilo de lista y usarlo en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| listStyle | [Style](../../com.aspose.words/style/) | El estilo de lista. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### add(int listTemplate) {#add-int}
```
public List add(int listTemplate)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### addCopy(List srcList) {#addCopy-com.aspose.words.List}
```
public List addCopy(List srcList)
```


Crea una nueva lista copiando la lista especificada y agregándola a la colección de listas del documento.

 **Remarks:** 

La lista origen puede provenir de cualquier documento. Si la lista origen pertenece a un documento diferente, se crea una copia de la lista y se agrega al documento actual.

Si la lista origen es una referencia o una definición de un estilo de lista, la lista recién creada no está relacionada con el estilo de lista original.

 **Examples:** 

Muestra cómo reiniciar la numeración en una lista copiando una lista.

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

Muestra cómo crear un documento con una muestra de todas las listas de otro documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcList | [List](../../com.aspose.words/list/) | La lista origen de la cual copiar. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### addSingleLevelList(int listTemplate) {#addSingleLevelList-int}
```
public List addSingleLevelList(int listTemplate)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### get(int index) {#get-int}
```
public List get(int index)
```


Obtiene una lista por índice.

 **Examples:** 

Muestra cómo aplicar el formato de lista de una lista existente a una colección de párrafos.

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

Muestra cómo verificar las propiedades del documento propietario de las listas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[List](../../com.aspose.words/list/) - A list by index.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el recuento de listas numeradas y con viñetas en el documento.

 **Examples:** 

Muestra cómo verificar las propiedades del documento propietario de las listas.

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
int - El recuento de listas numeradas y con viñetas en el documento.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Obtiene el documento propietario.

 **Examples:** 

Muestra cómo verificar las propiedades del documento propietario de las listas.

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


Obtiene una lista mediante un identificador de lista.

 **Remarks:** 

Normalmente no necesita usar este método. La mayor parte del tiempo aplica el formato de lista a los párrafos simplemente configurando la propiedad [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) del objeto [ListFormat](../../com.aspose.words/listformat/).

 **Examples:** 

Muestra cómo verificar las propiedades del documento propietario de las listas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| listId | int | El identificador de la lista. |

**Returns:**
[List](../../com.aspose.words/list/) - Returns the list object. Returns  null  if a list with the specified identifier was not found.
### iterator() {#iterator}
```
public Iterator iterator()
```


Obtiene el objeto enumerador que enumerará las listas en el documento.

 **Examples:** 

Muestra cómo crear un documento con una muestra de todas las listas de otro documento.

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
