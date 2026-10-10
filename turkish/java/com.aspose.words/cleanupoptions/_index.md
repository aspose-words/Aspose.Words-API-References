---
title: "CleanupOptions"
linktitle: "CleanupOptions"
second_title: "Aspose.Words Java için"
description: "Java'da belge temizleme seçeneklerini belirtmeye olanak tanır."
type: docs
weight: 103
url: /tr/java/com.aspose.words/cleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class CleanupOptions
```

Belge temizliği için seçenekleri belirtmeye izin verir.

Daha fazla bilgi için, [ Belgeyi Temizleme ][Belgeyi Temizleme] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir belgeden kullanılmayan tüm özel stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```


[Clean Up a Document]: https://docs.aspose.com/words/java/clean-up-a-document/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDuplicateStyle()](#getDuplicateStyle) | Belgeden yinelenen stillerin kaldırılıp kaldırılmayacağını gösteren bir bayrağı alır/ayarlar. |
| [getUnusedBuiltinStyles()](#getUnusedBuiltinStyles) | Kullanılmayan [Style.getBuiltIn()](../../com.aspose.words/style/\#getBuiltIn) stillerin belgeden kaldırılması gerektiğini belirtir. |
| [getUnusedLists()](#getUnusedLists) | Kullanılmayan liste ve liste tanımlarının belgeden kaldırılıp kaldırılmayacağını belirtir. |
| [getUnusedStyles()](#getUnusedStyles) | Kullanılmayan stillerin belgeden kaldırılıp kaldırılmayacağını belirtir. |
| [setDuplicateStyle(boolean value)](#setDuplicateStyle-boolean) | Belgeden yinelenen stillerin kaldırılıp kaldırılmayacağını gösteren bir bayrağı alır/ayarlar. |
| [setUnusedBuiltinStyles(boolean value)](#setUnusedBuiltinStyles-boolean) | Kullanılmayan [Style.getBuiltIn()](../../com.aspose.words/style/\#getBuiltIn) stillerin belgeden kaldırılması gerektiğini belirtir. |
| [setUnusedLists(boolean value)](#setUnusedLists-boolean) | Kullanılmayan liste ve liste tanımlarının belgeden kaldırılıp kaldırılmayacağını belirtir. |
| [setUnusedStyles(boolean value)](#setUnusedStyles-boolean) | Kullanılmayan stillerin belgeden kaldırılıp kaldırılmayacağını belirtir. |
### getDuplicateStyle() {#getDuplicateStyle}
```
public boolean getDuplicateStyle()
```


Belgeden yinelenen stillerin kaldırılıp kaldırılmayacağını gösteren bir bayrağı alır/ayarlar. Varsayılan değer false.

 **Examples:** 

Belgeden yinelenen stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 // Add two styles to the document with identical properties,
 // but different names. The second style is considered a duplicate of the first.
 Style myStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 Style duplicateStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle2");
 duplicateStyle.getFont().setSize(14.0);
 duplicateStyle.getFont().setName("Courier New");
 duplicateStyle.getFont().setColor(Color.BLUE);

 Assert.assertEquals(6, doc.getStyles().getCount());

 // Apply both styles to different paragraphs within the document.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 builder.getParagraphFormat().setStyleName(duplicateStyle.getName());
 builder.writeln("Hello again!");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(duplicateStyle, paragraphs.get(1).getParagraphFormat().getStyle());

 // Configure a CleanOptions object, then call the Cleanup method to substitute all duplicate styles
 // with the original and remove the duplicates from the document.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setDuplicateStyle(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(5, doc.getStyles().getCount());
 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(myStyle, paragraphs.get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getUnusedBuiltinStyles() {#getUnusedBuiltinStyles}
```
public boolean getUnusedBuiltinStyles()
```


Kullanılmayan [Style.getBuiltIn()](../../com.aspose.words/style/\#getBuiltIn) stillerin belgeden kaldırılması gerektiğini belirtir.

 **Examples:** 

Bir belgeden kullanılmayan tüm özel stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getUnusedLists() {#getUnusedLists}
```
public boolean getUnusedLists()
```


Belgeden kullanılmayan liste ve liste tanımlarının kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer true.

 **Examples:** 

Bir belgeden kullanılmayan tüm özel stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getUnusedStyles() {#getUnusedStyles}
```
public boolean getUnusedStyles()
```


Belgeden kullanılmayan stillerin kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer true.

 **Examples:** 

Bir belgeden kullanılmayan tüm özel stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### setDuplicateStyle(boolean value) {#setDuplicateStyle-boolean}
```
public void setDuplicateStyle(boolean value)
```


Belgeden yinelenen stillerin kaldırılıp kaldırılmayacağını gösteren bir bayrağı alır/ayarlar. Varsayılan değer false.

 **Examples:** 

Belgeden yinelenen stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 // Add two styles to the document with identical properties,
 // but different names. The second style is considered a duplicate of the first.
 Style myStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 Style duplicateStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle2");
 duplicateStyle.getFont().setSize(14.0);
 duplicateStyle.getFont().setName("Courier New");
 duplicateStyle.getFont().setColor(Color.BLUE);

 Assert.assertEquals(6, doc.getStyles().getCount());

 // Apply both styles to different paragraphs within the document.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 builder.getParagraphFormat().setStyleName(duplicateStyle.getName());
 builder.writeln("Hello again!");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(duplicateStyle, paragraphs.get(1).getParagraphFormat().getStyle());

 // Configure a CleanOptions object, then call the Cleanup method to substitute all duplicate styles
 // with the original and remove the duplicates from the document.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setDuplicateStyle(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(5, doc.getStyles().getCount());
 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(myStyle, paragraphs.get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setUnusedBuiltinStyles(boolean value) {#setUnusedBuiltinStyles-boolean}
```
public void setUnusedBuiltinStyles(boolean value)
```


Kullanılmayan [Style.getBuiltIn()](../../com.aspose.words/style/\#getBuiltIn) stillerin belgeden kaldırılması gerektiğini belirtir.

 **Examples:** 

Bir belgeden kullanılmayan tüm özel stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setUnusedLists(boolean value) {#setUnusedLists-boolean}
```
public void setUnusedLists(boolean value)
```


Belgeden kullanılmayan liste ve liste tanımlarının kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer true.

 **Examples:** 

Bir belgeden kullanılmayan tüm özel stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setUnusedStyles(boolean value) {#setUnusedStyles-boolean}
```
public void setUnusedStyles(boolean value)
```


Belgeden kullanılmayan stillerin kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer true.

 **Examples:** 

Bir belgeden kullanılmayan tüm özel stillerin nasıl kaldırılacağını gösterir.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

