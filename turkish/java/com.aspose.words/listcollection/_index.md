---
title: "ListCollection"
linktitle: "ListCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgede kullanılan madde işaretli ve numaralı listelerin biçimlendirmesini depolar ve yönetir."
type: docs
weight: 426
url: /tr/java/com.aspose.words/listcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListCollection implements Cloneable, Iterable
```

Bir belgede kullanılan madde işaretli ve numaralı listelerin biçimlendirmesini depolar ve yönetir.

Daha fazla bilgi için, [ Working with Lists ][Working with Lists] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Microsoft Word belgesindeki bir liste, bir dizi liste biçimlendirme özelliğidir. Listelerin biçimlendirmesi, metin paragraflarından ayrı olarak [ListCollection](../../com.aspose.words/listcollection/) koleksiyonunda depolanır.

Bu sınıfın nesnelerini oluşturmazsınız. Her belge için her zaman yalnızca bir [ListCollection](../../com.aspose.words/listcollection/) nesnesi bulunur ve bu nesne [DocumentBase.getLists()](../../com.aspose.words/documentbase/\#getLists) özelliği aracılığıyla erişilebilir.

Önceden tanımlı bir liste şablonuna ya da bir liste stiline dayalı yeni bir liste oluşturmak için, [add(com.aspose.words.Style)](../../com.aspose.words/listcollection/\#add-com.aspose.words.Style) yöntemini kullanın.

Mevcut bir listeye aynı biçimlendirmeye sahip yeni bir liste oluşturmak için, [addCopy(com.aspose.words.List)](../../com.aspose.words/listcollection/\#addCopy-com.aspose.words.List) metodunu kullanın.

Bir paragrafı madde işaretli ya da numaralı yapmak için, bir paragrafın [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) özelliğine bir [List](../../com.aspose.words/list/) nesnesi atayarak liste biçimlendirmesi uygulamanız gerekir.

Bir paragraftan liste biçimlendirmesini kaldırmak için, [ListFormat.removeNumbers()](../../com.aspose.words/listformat/\#removeNumbers) metodunu kullanın.

WordprocessingML hakkında biraz biliyorsanız, "list" ve "list definition" için ayrı kavramlar tanımladığını da bilmiş olabilirsiniz. Bu, liste biçimlendirmesinin bir Microsoft Word belgesinde düşük seviyede nasıl depolandığıyla tam olarak eşleşir. Liste tanımı bir "schema" gibidir ve liste, bir liste tanımının örneği gibidir.

Programlama modelini basitleştirmek için, Aspose.Words, Microsoft Word'ün kullanıcı arayüzünde yaptığı gibi, liste ile liste tanımı arasındaki farkı gizler. Bu, Microsoft Word dosya formatının gereksinimlerini karşılamak için düşük seviyeli nesneler oluşturmak yerine belgenizin nasıl görünmesini istediğinize daha çok odaklanmanızı sağlar.

Aspose.Words'ün mevcut sürümünde listeler oluşturulduktan sonra silinmeleri mümkün değildir. Bu, kullanıcının liste tanımları üzerinde açık bir kontrolü olmadığı Microsoft Word'e benzer.

 **Examples:** 

Liste seviyeleriyle nasıl çalışılacağını gösterir.

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

Bir listeyi kopyalayarak listede numaralandırmayı nasıl yeniden başlatacağını gösterir.

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

Başka bir belgeden tüm listelerin örneklerini içeren bir belge nasıl oluşturulur gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(Style listStyle)](#add-com.aspose.words.Style) | Bir liste stiline referans veren yeni bir liste oluşturur ve bu listeyi belgedeki listeler koleksiyonuna ekler. |
| [add(int listTemplate)](#add-int) |  |
| [addCopy(List srcList)](#addCopy-com.aspose.words.List) | Belirtilen listeyi kopyalayarak yeni bir liste oluşturur ve bu listeyi belgedeki listeler koleksiyonuna ekler. |
| [addSingleLevelList(int listTemplate)](#addSingleLevelList-int) |  |
| [get(int index)](#get-int) | Bir listeyi indeksine göre alır. |
| [getCount()](#getCount) | Belgedeki numaralı ve madde işaretli listelerin sayısını alır. |
| [getDocument()](#getDocument) | Sahip belgeyi alır. |
| [getListByListId(int listId)](#getListByListId-int) | Bir listeyi liste tanımlayıcısına göre alır. |
| [iterator()](#iterator) | Belgedeki listeleri yineleyecek enumerator nesnesini alır. |
### add(Style listStyle) {#add-com.aspose.words.Style}
```
public List add(Style listStyle)
```


Bir liste stiline referans veren yeni bir liste oluşturur ve bu listeyi belgedeki listeler koleksiyonuna ekler.

 **Remarks:** 

Yeni oluşturulan liste, liste stiline referans verir. Liste stilinin özelliklerini değiştirirseniz, bu değişiklik listenin özelliklerine yansır. Tersine, listenin özelliklerini değiştirirseniz, bu değişiklik liste stilinin özelliklerine yansır.

 **Examples:** 

Bir liste stili nasıl oluşturulur ve bir belgede nasıl kullanılır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| listStyle | [Style](../../com.aspose.words/style/) | Liste stili. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### add(int listTemplate) {#add-int}
```
public List add(int listTemplate)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### addCopy(List srcList) {#addCopy-com.aspose.words.List}
```
public List addCopy(List srcList)
```


Belirtilen listeyi kopyalayarak yeni bir liste oluşturur ve bu listeyi belgedeki listeler koleksiyonuna ekler.

 **Remarks:** 

Kaynak liste herhangi bir belgeden olabilir. Kaynak liste farklı bir belgeye aitse, listenin bir kopyası oluşturulur ve geçerli belgeye eklenir.

Kaynak liste bir liste stiline referans veya tanım ise, yeni oluşturulan liste orijinal liste stiliyle ilişkili değildir.

 **Examples:** 

Bir listeyi kopyalayarak listede numaralandırmayı nasıl yeniden başlatacağını gösterir.

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

Başka bir belgeden tüm listelerin örneklerini içeren bir belge nasıl oluşturulur gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcList | [List](../../com.aspose.words/list/) | Kopyalanacak kaynak liste. |

**Returns:**
[List](../../com.aspose.words/list/) - The newly created list.
### addSingleLevelList(int listTemplate) {#addSingleLevelList-int}
```
public List addSingleLevelList(int listTemplate)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list/)
### get(int index) {#get-int}
```
public List get(int index)
```


Bir listeyi indeksine göre alır.

 **Examples:** 

Mevcut bir listenin liste biçimlendirmesinin bir paragraf koleksiyonuna nasıl uygulanacağını gösterir.

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

Listelerin sahip belge özelliklerinin nasıl doğrulanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

**Returns:**
[List](../../com.aspose.words/list/) - A list by index.
### getCount() {#getCount}
```
public int getCount()
```


Belgedeki numaralı ve madde işaretli listelerin sayısını alır.

 **Examples:** 

Listelerin sahip belge özelliklerinin nasıl doğrulanacağını gösterir.

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
int - Belgedeki numaralı ve madde işaretli listelerin sayısı.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Sahip belgeyi alır.

 **Examples:** 

Listelerin sahip belge özelliklerinin nasıl doğrulanacağını gösterir.

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


Bir listeyi liste tanımlayıcısına göre alır.

 **Remarks:** 

Genellikle bu metodu kullanmanız gerekmez. Çoğu zaman, bir paragrafın üzerine liste biçimlendirmesini sadece [ListFormat.getList()](../../com.aspose.words/listformat/\#getList) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) özelliğini [ListFormat](../../com.aspose.words/listformat/) nesnesine ayarlayarak uygularsınız.

 **Examples:** 

Listelerin sahip belge özelliklerinin nasıl doğrulanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| listId | int | Liste tanımlayıcısı. |

**Returns:**
[List](../../com.aspose.words/list/) - Returns the list object. Returns  null  if a list with the specified identifier was not found.
### iterator() {#iterator}
```
public Iterator iterator()
```


Belgedeki listeleri yineleyecek enumerator nesnesini alır.

 **Examples:** 

Başka bir belgeden tüm listelerin örneklerini içeren bir belge nasıl oluşturulur gösterir.

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
