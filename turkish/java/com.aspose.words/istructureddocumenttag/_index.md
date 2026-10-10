---
title: "IStructuredDocumentTag"
linktitle: "IStructuredDocumentTag"
second_title: "Aspose.Words Java için"
description: "Java'da StructuredDocumentTag ve StructuredDocumentTagRangeStart için ortak veri tanımlayan arayüz."
type: docs
weight: 785
url: /tr/java/com.aspose.words/istructureddocumenttag/
---
```
public interface IStructuredDocumentTag
```

Ortak veri tanımlamak için [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) ve [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/) arayüzü.

 **Examples:** 

Yapılandırılmış belge etiketini nasıl kaldıracağınızı gösterir, ancak içeriği korur.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This collection provides a unified interface for accessing ranged and non-ranged structured tags.
 StructuredDocumentTagCollection sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(5, sdts.getCount());

 // Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
 for (IStructuredDocumentTag sdt : sdts)
     if (sdt.getChildNodes(NodeType.ANY, false).getCount() > 0)
         sdt.removeSelfOnly();

 sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(0, sdts.getCount());
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAppearance()](#getAppearance) | Yapılandırılmış belge etiketinin görünümünü alır. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getColor()](#getColor) | Yapılandırılmış belge etiketinin rengini alır. |
| [getId()](#getId) | Bu **SDT** için benzersiz, yalnızca okunabilir, kalıcı sayısal kimliği belirtir. |
| [getLevel()](#getLevel) | Bu **SDT**'nin belge ağacında bulunduğu seviyeyi alır. |
| [getLockContentControl()](#getLockContentControl) | True olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'yi silmesini engeller. |
| [getLockContents()](#getLockContents) | True olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'nin içeriğini düzenlemesini engeller. |
| [getNode()](#getNode) | Bu arayüzü uygulayan Node nesnesini döndürür. |
| [getPlaceholder()](#getPlaceholder) | Bu SDT çalıştırma içeriği boş olduğunda gösterilmesi gereken yer tutucu metni içeren [BuildingBlock](../../com.aspose.words/buildingblock/) nesnesini alır; ilgili eşlenmiş XML öğesi, [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) öğesiyle veya [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) öğesi true olduğunda belirtilir. |
| [getPlaceholderName()](#getPlaceholderName) | [BuildingBlock](../../com.aspose.words/buildingblock/) içinde yer tutucu metni içeren adını alır veya ayarlar. |
| [getSdtType()](#getSdtType) | Bu **Structured document tag** tipini alır. |
| [getTag()](#getTag) | Mevcut SDT düğümüyle ilişkili bir etiketi belirtir. |
| [getTitle()](#getTitle) | Bu **SDT** ile ilişkili kullanıcı dostu adı belirtir. |
| [getWordOpenXML()](#getWordOpenXML) | Düğüm içinde bulunan XML'i [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) formatında temsil eden bir dizeyi alır. |
| [getXmlMapping()](#getXmlMapping) | Bu yapılandırılmış belge etiketinin, mevcut belgenin özel bir XML bölümündeki XML verisine eşlenmesini temsil eden bir nesneyi alır. |
| [isMultiSection()](#isMultiSection) | Bu örnek bir aralıklı (çok bölümlü) yapılandırılmış belge etiketi ise true döndürür. |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | Bu **SDT**'nin içeriğinin yer tutucu metin içerdiği (SDT içindeki normal metin içeriklerine karşı) yorumlanıp yorumlanmayacağını belirtir. |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | Bu **SDT**'nin içeriğinin yer tutucu metin içerdiği (SDT içindeki normal metin içeriklerine karşı) yorumlanıp yorumlanmayacağını belirtir. |
| [removeSelfOnly()](#removeSelfOnly) | Bu SDT düğümünü yalnızca kaldırır, ancak içeriğini belge ağacında tutar. |
| [setAppearance(int value)](#setAppearance-int) | Yapılandırılmış belge etiketinin görünümünü ayarlar. |
| [setColor(Color value)](#setColor-java.awt.Color) | Yapılandırılmış belge etiketinin rengini ayarlar. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | True olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'yi silmesini engeller. |
| [setLockContents(boolean value)](#setLockContents-boolean) | True olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'nin içeriğini düzenlemesini engeller. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | [BuildingBlock](../../com.aspose.words/buildingblock/) içinde yer tutucu metni içeren adını alır veya ayarlar. |
| [setTag(String value)](#setTag-java.lang.String) | Mevcut SDT düğümüyle ilişkili bir etiketi belirtir. |
| [setTitle(String value)](#setTitle-java.lang.String) | Bu **SDT** ile ilişkili kullanıcı dostu adı belirtir. |
### getAppearance() {#getAppearance}
```
public abstract int getAppearance()
```


Yapılandırılmış belge etiketinin görünümünü alır.

 **Examples:** 

İçeriğin etrafında etiketi nasıl göstereceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Returns:**
int - Yapılandırılmış belge etiketinin görünümü. Döndürülen değer, [SdtAppearance](../../com.aspose.words/sdtappearance/) sabitlerinden biridir.
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public abstract NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getColor() {#getColor}
```
public abstract Color getColor()
```


Yapılandırılmış belge etiketinin rengini alır.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
java.awt.Color - Yapılandırılmış belge etiketinin rengi.
### getId() {#getId}
```
public abstract int getId()
```


Bu **SDT** için benzersiz, yalnızca okunabilir, kalıcı sayısal kimliği belirtir.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int - İlgili  int  değeri.
### getLevel() {#getLevel}
```
public abstract int getLevel()
```


Bu **SDT**'nin belge ağacında bulunduğu seviyeyi alır.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int - Bu **SDT**'nin belge ağacında ortaya çıktığı seviye. Döndürülen değer, [MarkupLevel](../../com.aspose.words/markuplevel/) sabitlerinden biridir.
### getLockContentControl() {#getLockContentControl}
```
public abstract boolean getLockContentControl()
```


True olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'yi silmesini engeller.

 **Examples:** 

Yapılandırılmış belge etiketlerine düzenleme kısıtlamalarının nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getLockContents() {#getLockContents}
```
public abstract boolean getLockContents()
```


True olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'nin içeriğini düzenlemesini engeller.

 **Examples:** 

Yapılandırılmış belge etiketlerine düzenleme kısıtlamalarının nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getNode() {#getNode}
```
public abstract Node getNode()
```


Bu arayüzü uygulayan Node nesnesini döndürür.

**Returns:**
[Node](../../com.aspose.words/node/) - Node object that implements this interface.
### getPlaceholder() {#getPlaceholder}
```
public abstract BuildingBlock getPlaceholder()
```


Bu SDT çalıştırma içeriği boş olduğunda gösterilmesi gereken yer tutucu metni içeren [BuildingBlock](../../com.aspose.words/buildingblock/) nesnesini alır; ilgili eşlenmiş XML öğesi, [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) öğesiyle veya [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) öğesi true olduğunda belirtilir.

 **Remarks:** 

Null olabilir, bu da yer tutucunun bu Sdt için geçerli olmadığı anlamına gelir.

 **Examples:** 

Bir yapı bloğunun içeriğinin, yapılandırılmış belge etiketi için özel bir yer tutucu metin olarak nasıl kullanılacağını gösterir.

```

 Document doc = new Document();

 // Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
 // The contents that it will display by default are a "Click here to enter text." prompt.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // We can get the tag to display the contents of a building block instead of the default text.
 // First, add a building block with contents to the glossary document.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();

 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("Custom Placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().appendChild(new Body(glossaryDoc));
 substituteBlock.getFirstSection().getBody().appendParagraph("Custom placeholder text.");

 glossaryDoc.appendChild(substituteBlock);

 // Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
 tag.setPlaceholderName("Custom Placeholder");

 // If "PlaceholderName" refers to an existing block in the parent document's glossary document,
 // we will be able to verify the building block via the "Placeholder" property.
 Assert.assertEquals(substituteBlock, tag.getPlaceholder());

 // Set the "IsShowingPlaceholderText" property to "true" to treat the
 // structured document tag's current contents as placeholder text.
 // This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
 // Set the "IsShowingPlaceholderText" property to "false" to get the
 // structured document tag to treat its contents as text that a user has already entered.
 // Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
 tag.isShowingPlaceholderText(isShowingPlaceholderText);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
 
```

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock/) - The [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) element is true.
### getPlaceholderName() {#getPlaceholderName}
```
public abstract String getPlaceholderName()
```


[BuildingBlock](../../com.aspose.words/buildingblock/) içinde yer tutucu metni içeren adını alır veya ayarlar.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getSdtType() {#getSdtType}
```
public abstract int getSdtType()
```


Bu **Structured document tag** tipini alır.

**Returns:**
int - Bu **Structured document tag**'in türü. Döndürülen değer, [SdtType](../../com.aspose.words/sdttype/) sabitlerinden biridir.
### getTag() {#getTag}
```
public abstract String getTag()
```


Geçerli SDT düğümüyle ilişkili bir etiketi belirtir. Null olamaz.

 **Examples:** 

Düz metin kutusunda bir yapılandırılmış belge etiketi oluşturmanın ve görünümünü değiştirmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // Create a structured document tag that will contain plain text.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
 tag.setTitle("My plain text");
 tag.setColor(Color.MAGENTA);

 // Set a tag for this structured document tag, which is obtainable
 // as an XML element named "tag", with the string below in its "@val" attribute.
 tag.setTag("MyPlainTextSDT");

 // Every structured document tag has a random unique ID.
 Assert.assertTrue(tag.getId() > 0);

 // Set the font for the text inside the structured document tag.
 tag.getContentsFont().setName("Arial");

 // Set the font for the text at the end of the structured document tag.
 // Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
 tag.getEndCharacterFont().setName("Arial Black");

 // By default, this is false and pressing enter while inside a structured document tag does nothing.
 // When set to true, our structured document tag can have multiple lines.

 // Set the "Multiline" property to "false" to only allow the contents
 // of this structured document tag to span a single line.
 // Set the "Multiline" property to "true" to allow the tag to contain multiple lines of content.
 tag.setMultiline(true);

 // Set the "Appearance" property to "SdtAppearance.Tags" to show tags around content.
 // By default structured document tag shows as BoundingBox.
 tag.setAppearance(SdtAppearance.TAGS);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 // Insert a clone of our structured document tag in a new paragraph.
 StructuredDocumentTag tagClone = (StructuredDocumentTag) tag.deepClone(true);
 builder.insertParagraph();
 builder.insertNode(tagClone);

 // Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
 tagClone.removeSelfOnly();

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlainText.docx");
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getTitle() {#getTitle}
```
public abstract String getTitle()
```


Bu **SDT** ile ilişkili dostane adı belirtir. Null olamaz.

 **Examples:** 

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getWordOpenXML() {#getWordOpenXML}
```
public abstract String getWordOpenXML()
```


Düğüm içinde bulunan XML'i [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) formatında temsil eden bir dizeyi alır.

 **Examples:** 

Düğüm içinde FlatOpc formatında bulunan XML'in nasıl alınacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 List tags = Arrays.stream(doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true).toArray())
         .filter(StructuredDocumentTag.class::isInstance)
         .map(StructuredDocumentTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertTrue(tags.get(0).getWordOpenXML()
         .contains(
                 ""));
 
```

**Returns:**
java.lang.String - Düğüm içinde [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) formatında bulunan XML'i temsil eden bir dize.
### getXmlMapping() {#getXmlMapping}
```
public abstract XmlMapping getXmlMapping()
```


Bu yapılandırılmış belge etiketinin, mevcut belgenin özel bir XML bölümündeki XML verisine eşlenmesini temsil eden bir nesneyi alır.

 **Remarks:** 

Bu nesnenin [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping/\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String) yöntemini, bir yapılandırılmış belge etiketini XML verisine eşlemek için kullanabilirsiniz.

 **Examples:** 

Özel XML verileriyle bir yapılandırılmış belge etiketi oluşturmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // Construct an XML part that contains data and add it to the document's collection.
 // If we enable the "Developer" tab in Microsoft Word,
 // we can find elements from this collection in the "XML Mapping Pane", along with a few default elements.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 Assert.assertEquals(xmlPart.getData(), xmlPartContent.getBytes());
 Assert.assertEquals(xmlPart.getId(), xmlPartId);

 // Below are two ways to refer to XML parts.
 // 1 -  By an index in the custom XML part collection:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().get(0));

 // 2 -  By GUID:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().getById(xmlPartId));

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone a part, and then insert it into the collection.
 CustomXmlPart xmlPartClone = xmlPart.deepClone();
 xmlPartClone.setId(UUID.randomUUID().toString());
 doc.getCustomXmlParts().add(xmlPartClone);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 2);

 // Iterate through the collection and print the contents of each part.
 Iterator enumerator = doc.getCustomXmlParts().iterator();
 int index = 0;
 while (enumerator.hasNext()) {
     CustomXmlPart customXmlPart = enumerator.next();
     System.out.println(MessageFormat.format("XML part index {0}, ID: {1}", index, customXmlPart.getId()));
     System.out.println(MessageFormat.format("\tContent: {0}", customXmlPart.getData()));
     index++;
 }

 // Use the "RemoveAt" method to remove the cloned part by index.
 doc.getCustomXmlParts().removeAt(1);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 1);

 // Clone the XML parts collection, and then use the "Clear" method to remove all its elements at once.
 CustomXmlPartCollection customXmlParts = doc.getCustomXmlParts().deepClone();
 customXmlParts.clear();

 // Create a structured document tag that will display our part's contents and insert it into the document body.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[1]", "");

 doc.getFirstSection().getBody().appendChild(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CustomXml.docx");
 
```

**Returns:**
[XmlMapping](../../com.aspose.words/xmlmapping/) - An object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document.
### isMultiSection() {#isMultiSection}
```
public abstract boolean isMultiSection()
```


Bu örnek bir aralıklı (çok bölümlü) yapılandırılmış belge etiketi ise true döndürür.

 **Examples:** 

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Returns:**
boolean - Bu örnek bir aralıklı (çok bölümlü) yapılandırılmış belge etiketi ise doğru.
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public abstract boolean isShowingPlaceholderText()
```


Bu **SDT**'nin içeriğinin yer tutucu metin içerdiği (SDT içindeki normal metin içeriklerine karşı) yorumlanıp yorumlanmayacağını belirtir.

true olarak ayarlanırsa, bu durum belge açıldığında (yer tutucu metni göstererek) devam eder.

 **Examples:** 

Bir yapı bloğunun içeriğinin, yapılandırılmış belge etiketi için özel bir yer tutucu metin olarak nasıl kullanılacağını gösterir.

```

 Document doc = new Document();

 // Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
 // The contents that it will display by default are a "Click here to enter text." prompt.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // We can get the tag to display the contents of a building block instead of the default text.
 // First, add a building block with contents to the glossary document.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();

 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("Custom Placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().appendChild(new Body(glossaryDoc));
 substituteBlock.getFirstSection().getBody().appendParagraph("Custom placeholder text.");

 glossaryDoc.appendChild(substituteBlock);

 // Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
 tag.setPlaceholderName("Custom Placeholder");

 // If "PlaceholderName" refers to an existing block in the parent document's glossary document,
 // we will be able to verify the building block via the "Placeholder" property.
 Assert.assertEquals(substituteBlock, tag.getPlaceholder());

 // Set the "IsShowingPlaceholderText" property to "true" to treat the
 // structured document tag's current contents as placeholder text.
 // This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
 // Set the "IsShowingPlaceholderText" property to "false" to get the
 // structured document tag to treat its contents as text that a user has already entered.
 // Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
 tag.isShowingPlaceholderText(isShowingPlaceholderText);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean}
```
public abstract void isShowingPlaceholderText(boolean value)
```


Bu **SDT**'nin içeriğinin yer tutucu metin içerdiği (SDT içindeki normal metin içeriklerine karşı) yorumlanıp yorumlanmayacağını belirtir.

true olarak ayarlanırsa, bu durum belge açıldığında (yer tutucu metni göstererek) devam eder.

 **Examples:** 

Bir yapı bloğunun içeriğinin, yapılandırılmış belge etiketi için özel bir yer tutucu metin olarak nasıl kullanılacağını gösterir.

```

 Document doc = new Document();

 // Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
 // The contents that it will display by default are a "Click here to enter text." prompt.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // We can get the tag to display the contents of a building block instead of the default text.
 // First, add a building block with contents to the glossary document.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();

 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("Custom Placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().appendChild(new Body(glossaryDoc));
 substituteBlock.getFirstSection().getBody().appendParagraph("Custom placeholder text.");

 glossaryDoc.appendChild(substituteBlock);

 // Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
 tag.setPlaceholderName("Custom Placeholder");

 // If "PlaceholderName" refers to an existing block in the parent document's glossary document,
 // we will be able to verify the building block via the "Placeholder" property.
 Assert.assertEquals(substituteBlock, tag.getPlaceholder());

 // Set the "IsShowingPlaceholderText" property to "true" to treat the
 // structured document tag's current contents as placeholder text.
 // This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
 // Set the "IsShowingPlaceholderText" property to "false" to get the
 // structured document tag to treat its contents as text that a user has already entered.
 // Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
 tag.isShowingPlaceholderText(isShowingPlaceholderText);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### removeSelfOnly() {#removeSelfOnly}
```
public abstract void removeSelfOnly()
```


Bu SDT düğümünü yalnızca kaldırır, ancak içeriğini belge ağacında tutar.

 **Examples:** 

Yapılandırılmış belge etiketini nasıl kaldıracağınızı gösterir, ancak içeriği korur.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This collection provides a unified interface for accessing ranged and non-ranged structured tags.
 StructuredDocumentTagCollection sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(5, sdts.getCount());

 // Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
 for (IStructuredDocumentTag sdt : sdts)
     if (sdt.getChildNodes(NodeType.ANY, false).getCount() > 0)
         sdt.removeSelfOnly();

 sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(0, sdts.getCount());
 
```

### setAppearance(int value) {#setAppearance-int}
```
public abstract void setAppearance(int value)
```


Yapılandırılmış belge etiketinin görünümünü ayarlar.

 **Examples:** 

İçeriğin etrafında etiketi nasıl göstereceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Yapılandırılmış belge etiketinin görünümü. Değer, [SdtAppearance](../../com.aspose.words/sdtappearance/) sabitlerinden biri olmalıdır. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public abstract void setColor(Color value)
```


Yapılandırılmış belge etiketinin rengini ayarlar.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Yapılandırılmış belge etiketinin rengi. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public abstract void setLockContentControl(boolean value)
```


True olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'yi silmesini engeller.

 **Examples:** 

Yapılandırılmış belge etiketlerine düzenleme kısıtlamalarının nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setLockContents(boolean value) {#setLockContents-boolean}
```
public abstract void setLockContents(boolean value)
```


True olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'nin içeriğini düzenlemesini engeller.

 **Examples:** 

Yapılandırılmış belge etiketlerine düzenleme kısıtlamalarının nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public abstract void setPlaceholderName(String value)
```


[BuildingBlock](../../com.aspose.words/buildingblock/) içinde yer tutucu metni içeren adını alır veya ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setTag(String value) {#setTag-java.lang.String}
```
public abstract void setTag(String value)
```


Geçerli SDT düğümüyle ilişkili bir etiketi belirtir. Null olamaz.

 **Examples:** 

Düz metin kutusunda bir yapılandırılmış belge etiketi oluşturmanın ve görünümünü değiştirmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // Create a structured document tag that will contain plain text.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
 tag.setTitle("My plain text");
 tag.setColor(Color.MAGENTA);

 // Set a tag for this structured document tag, which is obtainable
 // as an XML element named "tag", with the string below in its "@val" attribute.
 tag.setTag("MyPlainTextSDT");

 // Every structured document tag has a random unique ID.
 Assert.assertTrue(tag.getId() > 0);

 // Set the font for the text inside the structured document tag.
 tag.getContentsFont().setName("Arial");

 // Set the font for the text at the end of the structured document tag.
 // Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
 tag.getEndCharacterFont().setName("Arial Black");

 // By default, this is false and pressing enter while inside a structured document tag does nothing.
 // When set to true, our structured document tag can have multiple lines.

 // Set the "Multiline" property to "false" to only allow the contents
 // of this structured document tag to span a single line.
 // Set the "Multiline" property to "true" to allow the tag to contain multiple lines of content.
 tag.setMultiline(true);

 // Set the "Appearance" property to "SdtAppearance.Tags" to show tags around content.
 // By default structured document tag shows as BoundingBox.
 tag.setAppearance(SdtAppearance.TAGS);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 // Insert a clone of our structured document tag in a new paragraph.
 StructuredDocumentTag tagClone = (StructuredDocumentTag) tag.deepClone(true);
 builder.insertParagraph();
 builder.insertNode(tagClone);

 // Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
 tagClone.removeSelfOnly();

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlainText.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public abstract void setTitle(String value)
```


Bu **SDT** ile ilişkili dostane adı belirtir. Null olamaz.

 **Examples:** 

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

