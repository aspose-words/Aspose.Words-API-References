---
title: "ViewOptions"
linktitle: "ViewOptions"
second_title: "Aspose.Words Java için"
description: "Microsoft Word'ün Java'da bir belgenin nasıl gösterileceğini kontrol eden çeşitli seçenekler sunar."
type: docs
weight: 714
url: /tr/java/com.aspose.words/viewoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ViewOptions implements Cloneable
```

Bir belgenin Microsoft Word'de nasıl gösterileceğini kontrol eden çeşitli seçenekler sağlar.

Daha fazla bilgi edinmek için [ Work with Options and Appearance of Word Documents ][Work with Options and Appearance of Word Documents] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma türünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```


[Work with Options and Appearance of Word Documents]: https://docs.aspose.com/words/java/work-with-word-document-options-and-appearance/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape) | Baskı düzeni görünümünde arka plan şeklinin görüntülenmesini kontrol eder. |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries) | Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır. |
| [getFormsDesign()](#getFormsDesign) | Belgenin form tasarım modunda olup olmadığını belirtir. |
| [getViewType()](#getViewType) | Microsoft Word'deki görünüm modunu kontrol eder. |
| [getZoomPercent()](#getZoomPercent) | Belgenizi görmek istediğiniz yüzde değerini alır. |
| [getZoomType()](#getZoomType) | Pencere boyutuna göre bir yakınlaştırma değeri alır. |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean) | Baskı düzeni görünümünde arka plan şeklinin görüntülenmesini kontrol eder. |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean) | Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır. |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean) | Belgenin form tasarım modunda olup olmadığını belirtir. |
| [setViewType(int value)](#setViewType-int) | Microsoft Word'deki görünüm modunu kontrol eder. |
| [setZoomPercent(int value)](#setZoomPercent-int) | Belgenizi görmek istediğiniz yüzde değerini ayarlar. |
| [setZoomType(int value)](#setZoomType-int) | Pencere boyutuna göre bir yakınlaştırma değeri ayarlar. |
### getDisplayBackgroundShape() {#getDisplayBackgroundShape}
```
public boolean getDisplayBackgroundShape()
```


Baskı düzeni görünümünde arka plan şeklinin görüntülenmesini kontrol eder.

 **Examples:** 

Görünüm seçeneklerinde belge arka plan görüntülerinin nasıl gizleneceğini/gösterileceğini gösterir.

```

 // Use an HTML string to create a new document with a flat background color.
 final String HTML =
         "\r\n                \r\n                    Hello world!\r\n                \r\n            ";

 Document doc = new Document(new ByteArrayInputStream(HTML.getBytes()));

 // The source for the document has a flat color background,
 // the presence of which will set the "DisplayBackgroundShape" flag to "true".
 Assert.assertTrue(doc.getViewOptions().getDisplayBackgroundShape());

 // Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
 // This may affect some text colors to improve visibility.
 // Set the "DisplayBackgroundShape" to "false" to not display the background color.
 doc.getViewOptions().setDisplayBackgroundShape(displayBackgroundShape);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayBackgroundShape.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries}
```
public boolean getDoNotDisplayPageBoundaries()
```


Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır.

 **Examples:** 

Görünüm seçeneklerinde dikey boşluk ve üstbilgi/altbilgilerin nasıl gizleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert content that spans across 3 pages.
 builder.writeln("Paragraph 1, Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 2, Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 3, Page 3.");

 // Insert a header and a footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("This is the footer.");

 // This document contains a small amount of content that takes up a few full pages worth of space.
 // Set the "DoNotDisplayPageBoundaries" flag to "true" to get older versions of Microsoft Word to omit headers,
 // footers, and much of the vertical whitespace when displaying our document.
 // Set the "DoNotDisplayPageBoundaries" flag to "false" to get older versions of Microsoft Word
 // to normally display our document.
 doc.getViewOptions().setDoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayPageBoundaries.doc");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getFormsDesign() {#getFormsDesign}
```
public boolean getFormsDesign()
```


Belgenin form tasarım modunda olup olmadığını belirtir.

 **Remarks:** 

Şu anda yalnızca WordML formatındaki belgeler için çalışır.

 **Examples:** 

Form tasarım modunun nasıl etkinleştirileceğini/devre dışı bırakılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "FormsDesign" property to "false" to keep forms design mode disabled.
 // Set the "FormsDesign" property to "true" to enable forms design mode.
 doc.getViewOptions().setFormsDesign(useFormsDesign);

 doc.save(getArtifactsDir() + "ViewOptions.FormsDesign.xml");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getViewType() {#getViewType}
```
public int getViewType()
```


Microsoft Word'deki görünüm modunu kontrol eder.

 **Remarks:** 

Aspose.Words bu seçeneği okuyup yazabilse de, kullanımı uygulamaya özeldir. Örneğin MS Word 2013 bu seçeneğin değerine saygı göstermez.

 **Examples:** 

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [ViewType](../../com.aspose.words/viewtype/) sabitlerinden biridir.
### getZoomPercent() {#getZoomPercent}
```
public int getZoomPercent()
```


Belgenizi görmek istediğiniz yüzde değerini alır.

 **Remarks:** 

Aspose.Words bu seçeneği okuyup yazabilse de, kullanımı uygulamaya özeldir. Örneğin MS Word 2013 bu seçeneğin değerine saygı göstermez.

 **Examples:** 

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Returns:**
int - Belgenizi görmek istediğiniz yüzde değeri.
### getZoomType() {#getZoomType}
```
public int getZoomType()
```


Pencere boyutuna göre bir yakınlaştırma değeri alır.

 **Examples:** 

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma türünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```

**Returns:**
int - Pencere boyutuna göre bir yakınlaştırma değeri. Döndürülen değer, [ZoomType](../../com.aspose.words/zoomtype/) sabitlerinden biridir.
### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean}
```
public void setDisplayBackgroundShape(boolean value)
```


Baskı düzeni görünümünde arka plan şeklinin görüntülenmesini kontrol eder.

 **Examples:** 

Görünüm seçeneklerinde belge arka plan görüntülerinin nasıl gizleneceğini/gösterileceğini gösterir.

```

 // Use an HTML string to create a new document with a flat background color.
 final String HTML =
         "\r\n                \r\n                    Hello world!\r\n                \r\n            ";

 Document doc = new Document(new ByteArrayInputStream(HTML.getBytes()));

 // The source for the document has a flat color background,
 // the presence of which will set the "DisplayBackgroundShape" flag to "true".
 Assert.assertTrue(doc.getViewOptions().getDisplayBackgroundShape());

 // Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
 // This may affect some text colors to improve visibility.
 // Set the "DisplayBackgroundShape" to "false" to not display the background color.
 doc.getViewOptions().setDisplayBackgroundShape(displayBackgroundShape);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayBackgroundShape.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır.

 **Examples:** 

Görünüm seçeneklerinde dikey boşluk ve üstbilgi/altbilgilerin nasıl gizleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert content that spans across 3 pages.
 builder.writeln("Paragraph 1, Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 2, Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 3, Page 3.");

 // Insert a header and a footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("This is the footer.");

 // This document contains a small amount of content that takes up a few full pages worth of space.
 // Set the "DoNotDisplayPageBoundaries" flag to "true" to get older versions of Microsoft Word to omit headers,
 // footers, and much of the vertical whitespace when displaying our document.
 // Set the "DoNotDisplayPageBoundaries" flag to "false" to get older versions of Microsoft Word
 // to normally display our document.
 doc.getViewOptions().setDoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayPageBoundaries.doc");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setFormsDesign(boolean value) {#setFormsDesign-boolean}
```
public void setFormsDesign(boolean value)
```


Belgenin form tasarım modunda olup olmadığını belirtir.

 **Remarks:** 

Şu anda yalnızca WordML formatındaki belgeler için çalışır.

 **Examples:** 

Form tasarım modunun nasıl etkinleştirileceğini/devre dışı bırakılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "FormsDesign" property to "false" to keep forms design mode disabled.
 // Set the "FormsDesign" property to "true" to enable forms design mode.
 doc.getViewOptions().setFormsDesign(useFormsDesign);

 doc.save(getArtifactsDir() + "ViewOptions.FormsDesign.xml");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setViewType(int value) {#setViewType-int}
```
public void setViewType(int value)
```


Microsoft Word'deki görünüm modunu kontrol eder.

 **Remarks:** 

Aspose.Words bu seçeneği okuyup yazabilse de, kullanımı uygulamaya özeldir. Örneğin MS Word 2013 bu seçeneğin değerine saygı göstermez.

 **Examples:** 

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [ViewType](../../com.aspose.words/viewtype/) sabitlerinden biri olmalıdır. |

### setZoomPercent(int value) {#setZoomPercent-int}
```
public void setZoomPercent(int value)
```


Belgenizi görmek istediğiniz yüzde değerini ayarlar.

 **Remarks:** 

Aspose.Words bu seçeneği okuyup yazabilse de, kullanımı uygulamaya özeldir. Örneğin MS Word 2013 bu seçeneğin değerine saygı göstermez.

 **Examples:** 

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Belgenizi görmek istediğiniz yüzde değeri. |

### setZoomType(int value) {#setZoomType-int}
```
public void setZoomType(int value)
```


Pencere boyutuna göre bir yakınlaştırma değeri ayarlar.

 **Examples:** 

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma türünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Pencere boyutuna göre bir yakınlaştırma değeri. Değer, [ZoomType](../../com.aspose.words/zoomtype/) sabitlerinden biri olmalıdır. |

