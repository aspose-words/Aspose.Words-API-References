---
title: "TableStyle"
linktitle: "TableStyle"
second_title: "Aspose.Words Java için"
description: "Java'da bir tablo stilini temsil eder."
type: docs
weight: 660
url: /tr/java/com.aspose.words/tablestyle/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Style](../../com.aspose.words/style/)
```
public class TableStyle extends Style
```

Bir tablo stilini temsil eder.

Daha fazla bilgi için, [ Working with Tables ][Working with Tables] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [equals(Style style)](#equals-com.aspose.words.Style) | Belirtilen stil ile karşılaştırır. |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getAliases()](#getAliases) | Bu stilin tüm takma adlarını alır. |
| [getAlignment()](#getAlignment) | Tablo stili için hizalamayı belirtir. |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages) | Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin verilip verilmediğini gösteren bir bayrak alır. |
| [getAutomaticallyUpdate()](#getAutomaticallyUpdate) | Bu stilin uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir. |
| [getBaseStyleName()](#getBaseStyleName) | Bu stilin dayandığı stilin adını alır/ayarlar. |
| [getBorders()](#getBorders) | Stil için varsayılan hücre kenarlıklarının koleksiyonunu alır. |
| [getBottomPadding()](#getBottomPadding) | Tablo hücrelerinin içeriğinin altına eklenecek boşluk miktarını (puan cinsinden) alır. |
| [getBuiltIn()](#getBuiltIn) | Bu stil, MS Word'deki yerleşik stillerden biri ise doğru. |
| [getCellSpacing()](#getCellSpacing) | Hücreler arasındaki boşluk miktarını (puan cinsinden) alır. |
| [getColumnStripe()](#getColumnStripe) | Stil tek/çift sütun bantlamasını belirttiğinde bantlamaya dahil edilecek sütun sayısını alır. |
| [getConditionalStyles()](#getConditionalStyles) | Bu tablo stili için tanımlanabilecek koşullu stillerin koleksiyonu. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Sahip belgeyi alır. |
| [getFont()](#getFont) | Stilin karakter biçimlendirmesini alır. |
| [getLeftIndent()](#getLeftIndent) | Bir tablonun sol girintisini temsil eden değeri alır. |
| [getLeftPadding()](#getLeftPadding) | Tablo hücrelerinin içeriğinin soluna eklenecek boşluk miktarını (puan cinsinden) alır. |
| [getLinkedStyleName()](#getLinkedStyleName) | Bu stile bağlı olan [Style](../../com.aspose.words/style/) adını alır/ayarlar. |
| [getList()](#getList) | Bu liste stilinin biçimlendirmesini tanımlayan listeyi alır. |
| [getListFormat()](#getListFormat) | Bir paragraf stilinin liste biçimlendirme özelliklerine erişim sağlar. |
| [getLocked()](#getLocked) | Bu stilin kilitli olup olmadığını belirtir. |
| [getName()](#getName) | Stilin adını alır. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName) | Belirtilen stil ile biçimlendirilmiş bir paragraftan sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayarlar. |
| [getParagraphFormat()](#getParagraphFormat) | Stilin paragraf biçimlendirmesini alır. |
| [getPriority()](#getPriority) | Stiller görev bölmesinde sıralama önceliğini temsil eden tam sayı değerini alır/ayarlar. |
| [getRightPadding()](#getRightPadding) | Tablo hücrelerinin içeriğinin sağına eklenecek boşluk miktarını (puan cinsinden) alır. |
| [getRowStripe()](#getRowStripe) | Stil tek/çift satır bantlamasını belirttiğinde bantlamaya dahil edilecek satır sayısını alır. |
| [getSemiHidden()](#getSemiHidden) | Stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. |
| [getShading()](#getShading) | Tablo hücreleri için gölgelendirme biçimlendirmesine referans veren bir [Shading](../../com.aspose.words/shading/) nesnesi alır. |
| [getStyleIdentifier()](#getStyleIdentifier) | Yerel bağımsız bir yerleşik stil için stil tanımlayıcısını alır. |
| [getStyles()](#getStyles) | Bu stilin ait olduğu stil koleksiyonunu alır. |
| [getTopPadding()](#getTopPadding) | Tablo hücrelerinin içeriğinin üstüne eklenecek boşluk miktarını (puan cinsinden) alır. |
| [getType()](#getType) | Stil tipini alır (paragraf veya karakter). |
| [getUnhideWhenUsed()](#getUnhideWhenUsed) | Geçerli belgede kullanılan stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. |
| [getVerticalAlignment()](#getVerticalAlignment) | Hücreler için dikey hizalamayı belirtir. |
| [isHeading()](#isHeading) | Stil yerleşik Başlık stillerinden biri olduğunda doğru. |
| [isQuickStyle()](#isQuickStyle) | Bu stilin MS Word kullanıcı arayüzündeki Hızlı Stil galerisinde gösterilip gösterilmeyeceğini belirtir. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean) | Bu stilin MS Word kullanıcı arayüzündeki Hızlı Stil galerisinde gösterilip gösterilmeyeceğini belirtir. |
| [remove()](#remove) | Belirtilen stili belgeden kaldırır. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setAlignment(int value)](#setAlignment-int) | Tablo stili için hizalamayı belirtir. |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean) | Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin verilip verilmediğini gösteren bir bayrağı ayarlar. |
| [setAutomaticallyUpdate(boolean value)](#setAutomaticallyUpdate-boolean) | Bu stilin uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir. |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String) | Bu stilin dayandığı stilin adını alır/ayarlar. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBottomPadding(double value)](#setBottomPadding-double) | Tablo hücrelerinin içeriğinin altına eklenecek boşluk miktarını (puan cinsinden) ayarlar. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setCellSpacing(double value)](#setCellSpacing-double) | Hücreler arasındaki boşluk miktarını (puan cinsinden) ayarlar. |
| [setColumnStripe(int value)](#setColumnStripe-int) | Stil tek/çift sütun bantlamasını belirttiğinde bantlamaya dahil edilecek sütun sayısını ayarlar. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Bir tablonun sol girintisini temsil eden değeri ayarlar. |
| [setLeftPadding(double value)](#setLeftPadding-double) | Tablo hücrelerinin içeriğinin soluna eklenecek boşluk miktarını (puan cinsinden) ayarlar. |
| [setLinkedStyleName(String value)](#setLinkedStyleName-java.lang.String) | Bu stile bağlı olan [Style](../../com.aspose.words/style/) adını alır/ayarlar. |
| [setLocked(boolean value)](#setLocked-boolean) | Bu stilin kilitli olup olmadığını belirtir. |
| [setName(String value)](#setName-java.lang.String) | Stilin adını ayarlar. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String) | Belirtilen stil ile biçimlendirilmiş bir paragraftan sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayarlar. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setPriority(int value)](#setPriority-int) | Stiller görev bölmesinde sıralama önceliğini temsil eden tam sayı değerini alır/ayarlar. |
| [setRightPadding(double value)](#setRightPadding-double) | Tablo hücrelerinin içeriğinin sağına eklenecek boşluk miktarını (puan cinsinden) ayarlar. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRowStripe(int value)](#setRowStripe-int) | Stil tek/çift satır bantlamasını belirttiğinde bantlamaya dahil edilecek satır sayısını ayarlar. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setSemiHidden(boolean value)](#setSemiHidden-boolean) | Stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. |
| [setTopPadding(double value)](#setTopPadding-double) | Tablo hücrelerinin içeriğinin üstüne eklenecek boşluk miktarını (puan cinsinden) ayarlar. |
| [setUnhideWhenUsed(boolean value)](#setUnhideWhenUsed-boolean) | Geçerli belgede kullanılan stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Hücreler için dikey hizalamayı belirtir. |
### clearCellAttrs() {#clearCellAttrs}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style}
```
public boolean equals(Style style)
```


Belirtilen stil ile karşılaştırır. Stil kimlikleri yalnızca yerleşik stiller için karşılaştırılır. Stil varsayılanları karşılaştırmaya dahil edilmez. Temel stil, bağlı stil ve sonraki paragraf stili yinelemeli olarak karşılaştırılır.

 **Examples:** 

Stil takma adlarının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) |  |

**Returns:**
boolean
### fetchCellAttr(int key) {#fetchCellAttr-int}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAliases() {#getAliases}
```
public String[] getAliases()
```


Bu stilin tüm takma adlarını alır. Stil takma ada sahip değilse boş dize dizisi döndürülür.

 **Examples:** 

Stil takma adlarının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String[] - Bu stilin tüm takma adları.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Tablo stili için hizalamayı belirtir.

 **Remarks:** 

Varsayılan değer [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT) dir.

 **Examples:** 

Bir tablonun konumunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer [TableAlignment](../../com.aspose.words/tablealignment/) sabitlerinden biridir.
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages}
```
public boolean getAllowBreakAcrossPages()
```


Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin verilip verilmediğini gösteren bir bayrak alır.

 **Remarks:** 

Varsayılan değer  true .

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
boolean - Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin verilip verilmediğini gösteren bir bayrak.
### getAutomaticallyUpdate() {#getAutomaticallyUpdate}
```
public boolean getAutomaticallyUpdate()
```


Bu stilin uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir.

 **Remarks:** 

Özellik değeri doğru olarak ayarlanırsa, uygun paragraf biçimlendirmesi değiştiğinde MS Word mevcut stili otomatik olarak yeniden tanımlar.

AutomaticallyUpdate özelliği yalnızca paragraf stillerine uygulanabilir.

Varsayılan değer  false  dır.

 **Examples:** 

Özel bir stilin nasıl oluşturulacağını ve uygulanacağını gösterir.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getBaseStyleName() {#getBaseStyleName}
```
public String getBaseStyleName()
```


Bu stilin dayandığı stilin adını alır/ayarlar.

 **Remarks:** 

Bu, stil başka bir stile dayalı değilse boş bir dize olacaktır ve boş bir dizeye ayarlanabilir.

 **Examples:** 

Stil takma adlarının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Stil için varsayılan hücre kenarlıklarının koleksiyonunu alır.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - The collection of default cell borders for the style.
### getBottomPadding() {#getBottomPadding}
```
public double getBottomPadding()
```


Tablo hücrelerinin içeriğinin altına eklenecek boşluk miktarını (puan cinsinden) alır.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - Tablo hücrelerinin içeriğinin altına eklenecek boşluk miktarı (puan cinsinden).
### getBuiltIn() {#getBuiltIn}
```
public boolean getBuiltIn()
```


Bu stil, MS Word'deki yerleşik stillerden biri ise doğru.

 **Examples:** 

Özel stillerin yerleşik stillerden nasıl ayırt edileceğini gösterir.

```

 Document doc = new Document();

 // When we create a document using Microsoft Word, or programmatically using Aspose.Words,
 // the document will come with a collection of styles to apply to its text to modify its appearance.
 // We can access these built-in styles via the document's "Styles" collection.
 // These styles will all have the "BuiltIn" flag set to "true".
 Style style = doc.getStyles().get("Emphasis");

 Assert.assertTrue(style.getBuiltIn());

 // Create a custom style and add it to the collection.
 // Custom styles such as this will have the "BuiltIn" flag set to "false".
 style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 Assert.assertFalse(style.getBuiltIn());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getCellSpacing() {#getCellSpacing}
```
public double getCellSpacing()
```


Hücreler arasındaki boşluk miktarını (puan cinsinden) alır.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - Hücreler arasındaki boşluk miktarı (puan cinsinden).
### getColumnStripe() {#getColumnStripe}
```
public int getColumnStripe()
```


Stil tek/çift sütun bantlamasını belirttiğinde bantlamaya dahil edilecek sütun sayısını alır.

 **Examples:** 

Satırlar arasında değişen koşullu tablo stillerinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Returns:**
int - Stil tek/çift sütun bantlamasını belirttiğinde bantlamaya dahil edilecek sütun sayısı.
### getConditionalStyles() {#getConditionalStyles}
```
public ConditionalStyleCollection getConditionalStyles()
```


Bu tablo stili için tanımlanabilecek koşullu stillerin koleksiyonu.

 **Examples:** 

Bir tablonun belirli alan stilleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) - The corresponding [ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) value.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectCellAttr(int key) {#getDirectCellAttr-int}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
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
### getFont() {#getFont}
```
public Font getFont()
```


Stilin karakter biçimlendirmesini alır.

 **Remarks:** 

Liste stilleri için bu özellik  null  döndürür.

 **Examples:** 

Özel bir stilin nasıl oluşturulacağını ve uygulanacağını gösterir.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

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

**Returns:**
[Font](../../com.aspose.words/font/) - The character formatting of the style.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Bir tablonun sol girintisini temsil eden değeri alır.

 **Examples:** 

Bir tablonun konumunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Returns:**
double - Bir tablonun sol girintisini temsil eden değer.
### getLeftPadding() {#getLeftPadding}
```
public double getLeftPadding()
```


Tablo hücrelerinin içeriğinin soluna eklenecek boşluk miktarını (puan cinsinden) alır.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - Tablo hücrelerinin içeriğinin soluna eklenecek boşluk miktarı (puan cinsinden).
### getLinkedStyleName() {#getLinkedStyleName}
```
public String getLinkedStyleName()
```


Bu stil ile bağlantılı olan [Style](../../com.aspose.words/style/) adını alır/ayarlar. Bağlı stil yoksa boş dize döndürür.

 **Remarks:** 

Paragraf stilini karakter stiline ve tersine bağlamak yalnızca buna izin verilir.

Geçerli stil için LinkedStyleName ayarlandığında, otomatik olarak bağlı stil için de LinkedStyleName ayarlanır.

Boş dize atamak, daha önce bağlanmış stili bağlantısını kaldırmaya eşdeğerdir.

 **Examples:** 

Stil takma adlarının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

Stilleri birbirleriyle nasıl bağlayacağınızı gösterir.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getList() {#getList}
```
public List getList()
```


Bu liste stilinin biçimlendirmesini tanımlayan listeyi alır.

 **Remarks:** 

Bu özellik yalnızca liste stilleri için geçerlidir. Diğer stil türleri için bu özellik  null  döndürür.

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

**Returns:**
[List](../../com.aspose.words/list/) - The list that defines formatting of this list style.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Bir paragraf stilinin liste biçimlendirme özelliklerine erişim sağlar.

 **Remarks:** 

Bu özellik yalnızca paragraf stilleri için geçerlidir. Diğer stil türleri için bu özellik  null  döndürür.

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

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - The corresponding [ListFormat](../../com.aspose.words/listformat/) value.
### getLocked() {#getLocked}
```
public boolean getLocked()
```


Bu stilin kilitli olup olmadığını belirtir.

 **Examples:** 

Stilin nasıl kilitleneceğini gösterir.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getName() {#getName}
```
public String getName()
```


Stilin adını alır.

 **Remarks:** 

Boş dize olamaz.

Koleksiyonda zaten böyle bir isimde bir stil varsa, bu stil onu geçersiz kılar. Etkilenen tüm düğümler yeni stile referans verir.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - Stil adı.
### getNextParagraphStyleName() {#getNextParagraphStyleName}
```
public String getNextParagraphStyleName()
```


Belirtilen stil ile biçimlendirilmiş bir paragraftan sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayarlar.

 **Remarks:** 

Bu özellik Aspose.Words tarafından kullanılmaz. Sonraki paragraf stili, yalnızca belgeyi MS Word'de düzenlediğinizde otomatik olarak uygulanır.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Stilin paragraf biçimlendirmesini alır.

 **Remarks:** 

Karakter ve liste stilleri için bu özellik  null  döndürür.

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

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The paragraph formatting of the style.
### getPriority() {#getPriority}
```
public int getPriority()
```


Stiller görev bölmesinde sıralama önceliğini temsil eden tam sayı değerini alır/ayarlar.

 **Examples:** 

Bir stilin önceliğini belirleme ve gizleme yöntemini gösterir.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
int - İlgili  int  değeri.
### getRightPadding() {#getRightPadding}
```
public double getRightPadding()
```


Tablo hücrelerinin içeriğinin sağına eklenecek boşluk miktarını (puan cinsinden) alır.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - Tablo hücrelerinin içeriğinin sağına eklenecek boşluk miktarı (puan cinsinden).
### getRowStripe() {#getRowStripe}
```
public int getRowStripe()
```


Stil tek/çift satır bantlamasını belirttiğinde bantlamaya dahil edilecek satır sayısını alır.

 **Examples:** 

Satırlar arasında değişen koşullu tablo stillerinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Returns:**
int - Stil tek/çift satır bantlamasını belirttiğinde bantlamaya dahil edilecek satır sayısı.
### getSemiHidden() {#getSemiHidden}
```
public boolean getSemiHidden()
```


Stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmediğini alır/ayarlar.

 **Examples:** 

Bir stilin önceliğini belirleme ve gizleme yöntemini gösterir.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getShading() {#getShading}
```
public Shading getShading()
```


Tablo hücreleri için gölgelendirme biçimlendirmesine referans veren bir [Shading](../../com.aspose.words/shading/) nesnesi alır.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for table cells.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Yerel bağımsız bir yerleşik stil için stil tanımlayıcısını alır.

 **Remarks:** 

Kullanıcı tanımlı (özel) stiller için bu özellik [StyleIdentifier.USER](../../com.aspose.words/styleidentifier/\#USER) döndürür.

 **Examples:** 

TOC ile ilgili paragraflarda sağ sekme durağının konumunu nasıl değiştireceğinizi gösterir.

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
int - Yerel ayar bağımsız yerleşik stil tanımlayıcısı. Döndürülen değer [StyleIdentifier](../../com.aspose.words/styleidentifier/) sabitlerinden biridir.
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


Bu stilin ait olduğu stil koleksiyonunu alır.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection/) - The collection of styles this style belongs to.
### getTopPadding() {#getTopPadding}
```
public double getTopPadding()
```


Tablo hücrelerinin içeriğinin üstüne eklenecek boşluk miktarını (puan cinsinden) alır.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - Tablo hücrelerinin içeriğinin üstüne eklenecek boşluk miktarı (puan cinsinden).
### getType() {#getType}
```
public int getType()
```


Stil tipini alır (paragraf veya karakter).

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
int - Stil türü (paragraf veya karakter). Döndürülen değer [StyleType](../../com.aspose.words/styletype/) sabitlerinden biridir.
### getUnhideWhenUsed() {#getUnhideWhenUsed}
```
public boolean getUnhideWhenUsed()
```


Geçerli belgede kullanılan stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmeyeceğini alır/ayarlar. Kullanılan stil Stiller galerisinde gösterilmeliyse True olur.

 **Examples:** 

Bir stilin önceliğini belirleme ve gizleme yöntemini gösterir.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Hücreler için dikey hizalamayı belirtir.

 **Remarks:** 

Varsayılan değer [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/\#TOP) olarak ayarlanmıştır.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/) sabitlerinden biridir.
### isHeading() {#isHeading}
```
public boolean isHeading()
```


Stil yerleşik Başlık stillerinden biri olduğunda doğru.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isQuickStyle() {#isQuickStyle}
```
public boolean isQuickStyle()
```


Bu stilin MS Word kullanıcı arayüzündeki Hızlı Stil galerisinde gösterilip gösterilmeyeceğini belirtir.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isQuickStyle(boolean value) {#isQuickStyle-boolean}
```
public void isQuickStyle(boolean value)
```


Bu stilin MS Word kullanıcı arayüzündeki Hızlı Stil galerisinde gösterilip gösterilmeyeceğini belirtir.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### remove() {#remove}
```
public void remove()
```


Belirtilen stili belgeden kaldırır.

 **Remarks:** 

Stil kaldırma, belge modelinde aşağıdaki etkilere sahiptir:

 *  All references to the style are removed from corresponding paragraphs, runs and tables.
 *  If base style is removed its formatting is moved to child styles.
 *  If style to be deleted has a linked style, then both of these are deleted.

 **Examples:** 

Özel bir stilin nasıl oluşturulacağını ve uygulanacağını gösterir.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Tablo stili için hizalamayı belirtir.

 **Remarks:** 

Varsayılan değer [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT) dir.

 **Examples:** 

Bir tablonun konumunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [TableAlignment](../../com.aspose.words/tablealignment/) sabitlerinden biri olmalıdır. |

### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean}
```
public void setAllowBreakAcrossPages(boolean value)
```


Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin verilip verilmediğini gösteren bir bayrağı ayarlar.

 **Remarks:** 

Varsayılan değer  true .

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin verilip verilmediğini gösteren bir bayrak. |

### setAutomaticallyUpdate(boolean value) {#setAutomaticallyUpdate-boolean}
```
public void setAutomaticallyUpdate(boolean value)
```


Bu stilin uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir.

 **Remarks:** 

Özellik değeri doğru olarak ayarlanırsa, uygun paragraf biçimlendirmesi değiştiğinde MS Word mevcut stili otomatik olarak yeniden tanımlar.

AutomaticallyUpdate özelliği yalnızca paragraf stillerine uygulanabilir.

Varsayılan değer  false  dır.

 **Examples:** 

Özel bir stilin nasıl oluşturulacağını ve uygulanacağını gösterir.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String}
```
public void setBaseStyleName(String value)
```


Bu stilin dayandığı stilin adını alır/ayarlar.

 **Remarks:** 

Bu, stil başka bir stile dayalı değilse boş bir dize olacaktır ve boş bir dizeye ayarlanabilir.

 **Examples:** 

Stil takma adlarının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double}
```
public void setBottomPadding(double value)
```


Tablo hücrelerinin içeriğinin altına eklenecek boşluk miktarını (puan cinsinden) ayarlar.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Tablo hücrelerinin içeriğinin altına eklenmesi gereken boşluk miktarı (puan cinsinden). |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setCellSpacing(double value) {#setCellSpacing-double}
```
public void setCellSpacing(double value)
```


Hücreler arasındaki boşluk miktarını (puan cinsinden) ayarlar.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Hücreler arasındaki boşluk miktarı (puan cinsinden). |

### setColumnStripe(int value) {#setColumnStripe-int}
```
public void setColumnStripe(int value)
```


Stil tek/çift sütun bantlamasını belirttiğinde bantlamaya dahil edilecek sütun sayısını ayarlar.

 **Examples:** 

Satırlar arasında değişen koşullu tablo stillerinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Stil tek/çift sütun bantlamasını belirttiğinde bantlamaya dahil edilecek sütun sayısı. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Bir tablonun sol girintisini temsil eden değeri ayarlar.

 **Examples:** 

Bir tablonun konumunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Bir tablonun sol girintisini temsil eden değer. |

### setLeftPadding(double value) {#setLeftPadding-double}
```
public void setLeftPadding(double value)
```


Tablo hücrelerinin içeriğinin soluna eklenecek boşluk miktarını (puan cinsinden) ayarlar.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Tablo hücrelerinin içeriğinin soluna eklenmesi gereken boşluk miktarı (puan cinsinden). |

### setLinkedStyleName(String value) {#setLinkedStyleName-java.lang.String}
```
public void setLinkedStyleName(String value)
```


Bu stil ile bağlantılı olan [Style](../../com.aspose.words/style/) adını alır/ayarlar. Bağlı stil yoksa boş dize döndürür.

 **Remarks:** 

Paragraf stilini karakter stiline ve tersine bağlamak yalnızca buna izin verilir.

Geçerli stil için LinkedStyleName ayarlandığında, otomatik olarak bağlı stil için de LinkedStyleName ayarlanır.

Boş dize atamak, daha önce bağlanmış stili bağlantısını kaldırmaya eşdeğerdir.

 **Examples:** 

Stil takma adlarının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

Stilleri birbirleriyle nasıl bağlayacağınızı gösterir.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setLocked(boolean value) {#setLocked-boolean}
```
public void setLocked(boolean value)
```


Bu stilin kilitli olup olmadığını belirtir.

 **Examples:** 

Stilin nasıl kilitleneceğini gösterir.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Stilin adını ayarlar.

 **Remarks:** 

Boş dize olamaz.

Koleksiyonda zaten böyle bir isimde bir stil varsa, bu stil onu geçersiz kılar. Etkilenen tüm düğümler yeni stile referans verir.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Stil adı. |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String}
```
public void setNextParagraphStyleName(String value)
```


Belirtilen stil ile biçimlendirilmiş bir paragraftan sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayarlar.

 **Remarks:** 

Bu özellik Aspose.Words tarafından kullanılmaz. Sonraki paragraf stili, yalnızca belgeyi MS Word'de düzenlediğinizde otomatik olarak uygulanır.

 **Examples:** 

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setPriority(int value) {#setPriority-int}
```
public void setPriority(int value)
```


Stiller görev bölmesinde sıralama önceliğini temsil eden tam sayı değerini alır/ayarlar.

 **Examples:** 

Bir stilin önceliğini belirleme ve gizleme yöntemini gösterir.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setRightPadding(double value) {#setRightPadding-double}
```
public void setRightPadding(double value)
```


Tablo hücrelerinin içeriğinin sağına eklenecek boşluk miktarını (puan cinsinden) ayarlar.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Tablo hücrelerinin içeriğinin sağına eklenmesi gereken boşluk miktarı (puan cinsinden). |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setRowStripe(int value) {#setRowStripe-int}
```
public void setRowStripe(int value)
```


Stil tek/çift satır bantlamasını belirttiğinde bantlamaya dahil edilecek satır sayısını ayarlar.

 **Examples:** 

Satırlar arasında değişen koşullu tablo stillerinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Stil tek/çift satır bantlamasını belirttiğinde bantlamaya dahil edilecek satır sayısı. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setSemiHidden(boolean value) {#setSemiHidden-boolean}
```
public void setSemiHidden(boolean value)
```


Stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmediğini alır/ayarlar.

 **Examples:** 

Bir stilin önceliğini belirleme ve gizleme yöntemini gösterir.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setTopPadding(double value) {#setTopPadding-double}
```
public void setTopPadding(double value)
```


Tablo hücrelerinin içeriğinin üstüne eklenecek boşluk miktarını (puan cinsinden) ayarlar.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Tablo hücrelerinin içeriğinin üstüne eklenmesi gereken boşluk miktarı (puan cinsinden). |

### setUnhideWhenUsed(boolean value) {#setUnhideWhenUsed-boolean}
```
public void setUnhideWhenUsed(boolean value)
```


Geçerli belgede kullanılan stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmeyeceğini alır/ayarlar. Kullanılan stil Stiller galerisinde gösterilmeliyse True olur.

 **Examples:** 

Bir stilin önceliğini belirleme ve gizleme yöntemini gösterir.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Hücreler için dikey hizalamayı belirtir.

 **Remarks:** 

Varsayılan değer [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/\#TOP) olarak ayarlanmıştır.

 **Examples:** 

Bir tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/) sabitlerinden biri olmalıdır. |

