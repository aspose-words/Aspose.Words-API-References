---
title: "StyleCollection"
linktitle: "StyleCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgede yerleşik ve kullanıcı tanımlı stilleri temsil eden Style nesnelerinin bir koleksiyonu."
type: docs
weight: 642
url: /tr/java/com.aspose.words/stylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

Bir belgede yerleşik ve kullanıcı tanımlı stilleri temsil eden [Style](../../com.aspose.words/style/) nesnelerinin bir koleksiyonu.

Daha fazla bilgi için, [ Working with Styles and Themes ][Working with Styles and Themes] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```


[Working with Styles and Themes]: https://docs.aspose.com/words/java/working-with-styles-and-themes/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(int type, String name)](#add-int-java.lang.String) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style) | Bu koleksiyona bir stili kopyalar. |
| [clearQuickStyleGallery()](#clearQuickStyleGallery) | Hızlı Stil Galerisi panelinden tüm stilleri kaldırır. |
| [get(int index)](#get-int) | Bir stili indeksine göre alır. |
| [get(String name)](#get-java.lang.String) | Koleksiyondan bir stili alır. |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int) |  |
| [getCount()](#getCount) | Koleksiyondaki stil sayısını alır. |
| [getDefaultFont()](#getDefaultFont) | Belgenin varsayılan metin biçimlendirmesini alır. |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat) | Belgenin varsayılan paragraf biçimlendirmesini alır. |
| [getDocument()](#getDocument) | Sahip belgeyi alır. |
| [iterator()](#iterator) | Stilleri adlarının alfabetik sırasına göre sıralayacak bir enumeratör nesnesi alır. |
### add(int type, String name) {#add-int-java.lang.String}
```
public Style add(int type, String name)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tip | int |  |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### addCopy(Style style) {#addCopy-com.aspose.words.Style}
```
public Style addCopy(Style style)
```


Bu koleksiyona bir stili kopyalar.

 **Remarks:** 

Kopyalanacak stil aynı belgeye ya da farklı bir belgeye ait olabilir.

Bağlantılı stil kopyalanır.

Bu yöntem temel stilleri kopyalamaz.

Koleksiyon zaten aynı ada sahip bir stil içeriyorsa, yeni ad 0'dan başlayarak "\_number" eki eklenerek otomatik olarak oluşturulur; örn. "Normal\_0", "Heading 1\_1" vb. İçe aktarılan stilin adını değiştirmek için [Style.getName()](../../com.aspose.words/style/\#getName) / [Style.setName(java.lang.String)](../../com.aspose.words/style/\#setName-java.lang.String) ayarlayıcısını kullanın.

 **Examples:** 

Bir belgenin stilini nasıl klonlayacağını gösterir.

```

 Document doc = new Document();

 // The AddCopy method creates a copy of the specified style and
 // automatically generates a new name for the style, such as "Heading 1_0".
 Style newStyle = doc.getStyles().addCopy(doc.getStyles().get("Heading 1"));

 // Use the style's "Name" property to change the style's identifying name.
 newStyle.setName("My Heading 1");

 // Our document now has two identical looking styles with different names.
 // Changing settings of one of the styles do not affect the other.
 newStyle.getFont().setColor(Color.RED);

 Assert.assertEquals("My Heading 1", newStyle.getName());
 Assert.assertEquals("Heading 1", doc.getStyles().get("Heading 1").getName());

 Assert.assertEquals(doc.getStyles().get("Heading 1").getType(), newStyle.getType());
 Assert.assertEquals(doc.getStyles().get("Heading 1").getFont().getName(), newStyle.getFont().getName());
 Assert.assertEquals(doc.getStyles().get("Heading 1").getFont().getSize(), newStyle.getFont().getSize());
 Assert.assertNotEquals(doc.getStyles().get("Heading 1").getFont().getColor(), newStyle.getFont().getColor());
 
```

Bir belgeden başka bir belgeye stil nasıl içe aktarılır gösterir.

```

 Document srcDoc = new Document();

 // Create a custom style for the source document.
 Style srcStyle = srcDoc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 srcStyle.getFont().setColor(Color.RED);

 // Import the source document's custom style into the destination document.
 Document dstDoc = new Document();
 Style newStyle = dstDoc.getStyles().addCopy(srcStyle);

 // The imported style has an appearance identical to its source style.
 Assert.assertEquals("MyStyle", newStyle.getName());
 Assert.assertEquals(Color.RED.getRGB(), newStyle.getFont().getColor().getRGB());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) | Kopyalanacak stil. |

**Returns:**
[Style](../../com.aspose.words/style/) - Copied style ready for usage.
### clearQuickStyleGallery() {#clearQuickStyleGallery}
```
public void clearQuickStyleGallery()
```


Hızlı Stil Galerisi panelinden tüm stilleri kaldırır.

 **Examples:** 

Stil Galerisi panelinden stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 // Note that remove styles work only with DOCX format for now.
 doc.getStyles().clearQuickStyleGallery();

 doc.save(getArtifactsDir() + "Styles.RemoveStylesFromStyleGallery.docx");
 
```

### get(int index) {#get-int}
```
public Style get(int index)
```


Bir stili indeksine göre alır.

 **Examples:** 

Bir belgenin stil koleksiyonuna bir Style eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

**Returns:**
[Style](../../com.aspose.words/style/) - A style by index.
### get(String name) {#get-java.lang.String}
```
public Style get(String name)
```


Koleksiyondan bir stil alır.  Bir stili ad veya takma ad ile alır.

 **Remarks:** 

Büyük/küçük harfe duyarlıdır, verilen adla stil bulunamazsa  null  döndürür.

Eğer bu, henüz var olmayan yerleşik bir stilin İngilizce adıysa, otomatik olarak oluşturur.

 **Examples:** 

Belgenin sayfa yerleşimini ne zaman yeniden hesaplayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/) - The corresponding [Style](../../com.aspose.words/style/) value.
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int}
```
public Style getByStyleIdentifier(int sti)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sti | int |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyondaki stil sayısını alır.

 **Examples:** 

Bir belgenin stil koleksiyonuna bir Style eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Returns:**
int - Koleksiyondaki stil sayısı.
### getDefaultFont() {#getDefaultFont}
```
public Font getDefaultFont()
```


Belgenin varsayılan metin biçimlendirmesini alır.

 **Remarks:** 

Belirtmek gerekir ki belge geneli varsayılanlar Microsoft Word 2007'de tanıtıldı ve yalnızca OOXML formatlarında ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)) tam olarak desteklenir. Daha eski belge formatları bu özelliği sınırlı şekilde destekler ve yalnızca yazı tipi adları depolanabilir.

 **Examples:** 

Bir belgenin stil koleksiyonuna bir Style eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - Document default text formatting.
### getDefaultParagraphFormat() {#getDefaultParagraphFormat}
```
public ParagraphFormat getDefaultParagraphFormat()
```


Belgenin varsayılan paragraf biçimlendirmesini alır.

 **Remarks:** 

Belirtmek gerekir ki belge geneli varsayılanlar Microsoft Word 2007'de tanıtıldı ve yalnızca OOXML formatlarında ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)) tam olarak desteklenir. Daha eski belge formatları belge varsayılanı paragraf biçimlendirmesini desteklemez.

 **Examples:** 

Bir belgenin stil koleksiyonuna bir Style eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - Document default paragraph formatting.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Sahip belgeyi alır.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### iterator() {#iterator}
```
public Iterator iterator()
```


Stilleri adlarının alfabetik sırasına göre sıralayacak bir enumeratör nesnesi alır.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.util.Iterator
