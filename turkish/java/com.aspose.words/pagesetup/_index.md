---
title: "PageSetup"
linktitle: "PageSetup"
second_title: "Aspose.Words Java için"
description: "Java'da bir bölümün sayfa ayarı özelliklerini temsil eder."
type: docs
weight: 519
url: /tr/java/com.aspose.words/pagesetup/
---

**Inheritance:**
java.lang.Object
```
public class PageSetup
```

Bir bölümün sayfa ayarı özelliklerini temsil eder.

Daha fazla bilgi edinmek için, [ Working with Sections ][Working with Sections] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[PageSetup](../../com.aspose.words/pagesetup/) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

 **Examples:** 

Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma işlemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Sayfa ayarını varsayılan kağıt boyutu, kenar boşlukları ve yönlendirmeye sıfırlar. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [getBidi()](#getBidi) | Bu bölümün çift yönlü (karmaşık betikler) metin içerdiğini belirtir. |
| [getBorderAlwaysInFront()](#getBorderAlwaysInFront) | Sayfa kenarlığının kesişen metinler ve nesnelere göre nerede konumlandırıldığını belirtir. |
| [getBorderAppliesTo()](#getBorderAppliesTo) | Sayfa kenarlığının hangi sayfalarda basılacağını belirtir. |
| [getBorderDistanceFrom()](#getBorderDistanceFrom) | Belirtilen sayfa kenarlığının sayfanın kenarından mı yoksa çevrelediği metinden mi ölçüldüğünü gösteren bir değer alır. |
| [getBorderSurroundsFooter()](#getBorderSurroundsFooter) | Sayfa kenarlığının alt bilgiyi içerip içermediğini belirtir. |
| [getBorderSurroundsHeader()](#getBorderSurroundsHeader) | Sayfa kenarlığının üst bilgiyi içerip içermediğini belirtir. |
| [getBorders()](#getBorders) | Sayfa kenarlıklarının bir koleksiyonunu alır. |
| [getBottomMargin()](#getBottomMargin) | Sayfanın alt kenarı ile gövde metninin alt sınırı arasındaki mesafeyi (puan cinsinden) alır. |
| [getChapterPageSeparator()](#getChapterPageSeparator) | Bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakteri alır. |
| [getCharactersPerLine()](#getCharactersPerLine) | Belge ızgarasındaki satır başına karakter sayısını alır. |
| [getDifferentFirstPageHeaderFooter()](#getDifferentFirstPageHeaderFooter) | İlk sayfada farklı bir üst bilgi veya alt bilgi kullanılıyorsa doğru. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getEndnoteOptions()](#getEndnoteOptions) | Bu bölümde dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sunar. |
| [getFirstPageTray()](#getFirstPageTray) | Bir bölümün ilk sayfası için kullanılacak kağıt tepsisini (kova) alır. |
| [getFooterDistance()](#getFooterDistance) | Alt bilgi ile sayfanın alt kısmı arasındaki mesafeyi (puan cinsinden) alır. |
| [getFootnoteOptions()](#getFootnoteOptions) | Bu bölümde altnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sunar. |
| [getGutter()](#getGutter) | Belge ciltleme için kenarlığa eklenen ekstra boşluk miktarını alır. |
| [getHeaderDistance()](#getHeaderDistance) | Üst bilgi ile sayfanın üst kısmı arasındaki mesafeyi (puan cinsinden) alır. |
| [getHeadingLevelForChapter()](#getHeadingLevelForChapter) | Belgedeki bölüm başlıklarına uygulanan başlık düzeyi stilini alır. |
| [getLayoutMode()](#getLayoutMode) | Bu bölümün düzen modunu alır. |
| [getLeftMargin()](#getLeftMargin) | Sayfanın sol kenarı ile gövde metninin sol sınırı arasındaki mesafeyi (puan cinsinden) alır. |
| [getLineNumberCountBy()](#getLineNumberCountBy) | Satır numaraları için sayısal artışı alır. |
| [getLineNumberDistanceFromText()](#getLineNumberDistanceFromText) | Satır numaralarının sağ kenarı ile belgenin sol kenarı arasındaki mesafeyi alır. |
| [getLineNumberRestartMode()](#getLineNumberRestartMode) | Satır numaralandırmasının nasıl çalıştığını alır; yani yeni bir sayfa veya bölümün başında yeniden başlayıp başlamadığını veya sürekli devam edip etmediğini. |
| [getLineStartingNumber()](#getLineStartingNumber) | Başlangıç satır numarasını alır. |
| [getLinesPerPage()](#getLinesPerPage) | Belge ızgarasındaki sayfa başına satır sayısını alır. |
| [getMargins()](#getMargins) | Sayfanın önceden ayarlanmış [Margins](../../com.aspose.words/margins/) değerini alır. |
| [getMultiplePages()](#getMultiplePages) | Birden çok sayfalı belgeler için, belgenin bir kitapçık olarak ciltlenebilmesi için nasıl yazdırıldığını veya oluşturulduğunu alır veya ayarlar. |
| [getOddAndEvenPagesHeaderFooter()](#getOddAndEvenPagesHeaderFooter) | Belgenin tek sayfalar ve çift sayfalar için farklı üstbilgi ve altbilgi içeriyorsa True. |
| [getOrientation()](#getOrientation) | Sayfanın yönünü alır. |
| [getOtherPagesTray()](#getOtherPagesTray) | Bir bölümün ilk sayfası dışındaki tüm sayfalar için kullanılacak kağıt tepsisini (bin) alır. |
| [getPageHeight()](#getPageHeight) | Sayfanın yüksekliğini puan cinsinden alır. |
| [getPageNumberStyle()](#getPageNumberStyle) | Sayfa numarası biçimini alır. |
| [getPageStartingNumber()](#getPageStartingNumber) | Bölümün başlangıç sayfa numarasını alır. |
| [getPageWidth()](#getPageWidth) | Sayfanın genişliğini puan cinsinden alır. |
| [getPaperSize()](#getPaperSize) | Kağıt boyutunu alır. |
| [getRestartPageNumbering()](#getRestartPageNumbering) | Sayfa numaralandırması bölümün başında yeniden başlıyorsa True. |
| [getRightMargin()](#getRightMargin) | Sayfanın sağ kenarı ile metin gövdesinin sağ sınırı arasındaki mesafeyi (puan cinsinden) alır. |
| [getRtlGutter()](#getRtlGutter) | Microsoft Word'ün bölümü sağdan sola veya soldan sağa dillerine göre oluk (gutter) kullanıp kullanmadığını alır. |
| [getSectionStart()](#getSectionStart) | Belirtilen nesne için bölüm sonu tipini alır. |
| [getSheetsPerBooklet()](#getSheetsPerBooklet) | Her kitapçıkta bulunacak sayfa sayısını alır. |
| [getSuppressEndnotes()](#getSuppressEndnotes) | Dipnotların, dipnotları bastırmayan bir sonraki bölümün sonunda yazdırılması durumunda True. |
| [getTextColumns()](#getTextColumns) | Metin sütunları kümesini temsil eden bir koleksiyon döndürür. |
| [getTextOrientation()](#getTextOrientation) | Tüm sayfa için [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) belirtmeye izin verir. |
| [getTopMargin()](#getTopMargin) | Sayfanın üst kenarı ile metin gövdesinin üst sınırı arasındaki mesafeyi (puan cinsinden) alır. |
| [getVerticalAlignment()](#getVerticalAlignment) | Bir belge veya bölümdeki her sayfadaki metnin dikey hizalamasını alır. |
| [setBidi(boolean value)](#setBidi-boolean) | Bu bölümün çift yönlü (karmaşık betikler) metin içerdiğini belirtir. |
| [setBorderAlwaysInFront(boolean value)](#setBorderAlwaysInFront-boolean) | Sayfa kenarlığının kesişen metinler ve nesnelere göre nerede konumlandırıldığını belirtir. |
| [setBorderAppliesTo(int value)](#setBorderAppliesTo-int) | Sayfa kenarlığının hangi sayfalarda basılacağını belirtir. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBorderDistanceFrom(int value)](#setBorderDistanceFrom-int) | Belirtilen sayfa kenarlığının sayfanın kenarından mı yoksa çevresindeki metinden mi ölçüldüğünü gösteren bir değeri ayarlar. |
| [setBorderSurroundsFooter(boolean value)](#setBorderSurroundsFooter-boolean) | Sayfa kenarlığının alt bilgiyi içerip içermediğini belirtir. |
| [setBorderSurroundsHeader(boolean value)](#setBorderSurroundsHeader-boolean) | Sayfa kenarlığının üst bilgiyi içerip içermediğini belirtir. |
| [setBottomMargin(double value)](#setBottomMargin-double) | Sayfanın alt kenarı ile gövde metninin alt sınırı arasındaki mesafeyi (nokta cinsinden) ayarlar. |
| [setChapterPageSeparator(int value)](#setChapterPageSeparator-int) | Bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakteri ayarlar. |
| [setCharactersPerLine(int value)](#setCharactersPerLine-int) | Belge ızgarasındaki satır başına karakter sayısını ayarlar. |
| [setDifferentFirstPageHeaderFooter(boolean value)](#setDifferentFirstPageHeaderFooter-boolean) | İlk sayfada farklı bir üst bilgi veya alt bilgi kullanılıyorsa doğru. |
| [setFirstPageTray(int value)](#setFirstPageTray-int) | Bir bölümün ilk sayfası için kullanılacak kağıt tepsisini (kutusunu) ayarlar. |
| [setFooterDistance(double value)](#setFooterDistance-double) | Altbilgi ile sayfanın alt kısmı arasındaki mesafeyi (nokta cinsinden) ayarlar. |
| [setGutter(double value)](#setGutter-double) | Belge ciltleme için kenara eklenen ekstra boşluk miktarını ayarlar. |
| [setHeaderDistance(double value)](#setHeaderDistance-double) | Üstbilgi ile sayfanın üst kısmı arasındaki mesafeyi (nokta cinsinden) ayarlar. |
| [setHeadingLevelForChapter(int value)](#setHeadingLevelForChapter-int) | Belgedeki bölüm başlıklarına uygulanan başlık seviyesi stilini ayarlar. |
| [setLayoutMode(int value)](#setLayoutMode-int) | Bu bölümün yerleşim modunu ayarlar. |
| [setLeftMargin(double value)](#setLeftMargin-double) | Sayfanın sol kenarı ile gövde metninin sol sınırı arasındaki mesafeyi (nokta cinsinden) ayarlar. |
| [setLineNumberCountBy(int value)](#setLineNumberCountBy-int) | Satır numaraları için sayısal artışı ayarlar. |
| [setLineNumberDistanceFromText(double value)](#setLineNumberDistanceFromText-double) | Satır numaralarının sağ kenarı ile belgenin sol kenarı arasındaki mesafeyi ayarlar. |
| [setLineNumberRestartMode(int value)](#setLineNumberRestartMode-int) | Satır numaralandırmasının nasıl çalışacağını ayarlar; yani yeni bir sayfa ya da bölümün başında yeniden başlayıp başlamayacağını ya da sürekli devam edip etmeyeceğini belirler. |
| [setLineStartingNumber(int value)](#setLineStartingNumber-int) | Başlangıç satır numarasını ayarlar. |
| [setLinesPerPage(int value)](#setLinesPerPage-int) | Belge ızgarasındaki sayfa başına satır sayısını ayarlar. |
| [setMargins(int value)](#setMargins-int) | Sayfanın önceden ayarlanmış [Margins](../../com.aspose.words/margins/) ayarlarını belirler. |
| [setMultiplePages(int value)](#setMultiplePages-int) | Birden çok sayfalı belgeler için, belgenin bir kitapçık olarak ciltlenebilmesi için nasıl yazdırıldığını veya oluşturulduğunu alır veya ayarlar. |
| [setOddAndEvenPagesHeaderFooter(boolean value)](#setOddAndEvenPagesHeaderFooter-boolean) | Belgenin tek sayfalar ve çift sayfalar için farklı üstbilgi ve altbilgi içeriyorsa True. |
| [setOrientation(int value)](#setOrientation-int) | Sayfanın yönlendirmesini ayarlar. |
| [setOtherPagesTray(int value)](#setOtherPagesTray-int) | Bir bölümün ilk sayfası dışındaki tüm sayfalar için kullanılacak kağıt tepsisini (kutusunu) ayarlar. |
| [setPageHeight(double value)](#setPageHeight-double) | Sayfanın yüksekliğini nokta cinsinden ayarlar. |
| [setPageNumberStyle(int value)](#setPageNumberStyle-int) | Sayfa numarası biçimini ayarlar. |
| [setPageStartingNumber(int value)](#setPageStartingNumber-int) | Bölümün başlangıç sayfa numarasını ayarlar. |
| [setPageWidth(double value)](#setPageWidth-double) | Sayfanın genişliğini nokta cinsinden ayarlar. |
| [setPaperSize(int value)](#setPaperSize-int) | Kağıt boyutunu ayarlar. |
| [setRestartPageNumbering(boolean value)](#setRestartPageNumbering-boolean) | Sayfa numaralandırması bölümün başında yeniden başlıyorsa True. |
| [setRightMargin(double value)](#setRightMargin-double) | Sayfanın sağ kenarı ile gövde metninin sağ sınırı arasındaki mesafeyi (nokta cinsinden) ayarlar. |
| [setRtlGutter(boolean value)](#setRtlGutter-boolean) | Microsoft Word'ün bölüme, sağdan sola ya da soldan sağa dillerine göre oluk (gutter) kullanıp kullanmayacağını ayarlar. |
| [setSectionStart(int value)](#setSectionStart-int) | Belirtilen nesne için bölüm sonu tipini ayarlar. |
| [setSheetsPerBooklet(int value)](#setSheetsPerBooklet-int) | Her kitapçıkta dahil edilecek sayfa sayısını ayarlar. |
| [setSuppressEndnotes(boolean value)](#setSuppressEndnotes-boolean) | Dipnotların, dipnotları bastırmayan bir sonraki bölümün sonunda yazdırılması durumunda True. |
| [setTextOrientation(int value)](#setTextOrientation-int) | Tüm sayfa için [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) belirtmeye izin verir. |
| [setTopMargin(double value)](#setTopMargin-double) | Sayfanın üst kenarı ile gövde metninin üst sınırı arasındaki mesafeyi (nokta cinsinden) ayarlar. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Bir belge veya bölümdeki her sayfadaki metnin dikey hizalamasını ayarlar. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Sayfa ayarını varsayılan kağıt boyutu, kenar boşlukları ve yönlendirmeye sıfırlar.

 **Examples:** 

Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma işlemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

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
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Bu bölümün çift yönlü (karmaşık betikler) metin içerdiğini belirtir.

 **Remarks:** 

Doğru olduğunda, bu bölmedeki sütunlar sağdan sola yerleştirilir.

 **Examples:** 

Bir bölümdeki metin sütunlarının sırasını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getTextColumns().setCount(3);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 3.");

 // Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
 // The order of the columns will match the direction of the right-to-left text.
 // Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
 // The order of the columns will match the direction of the left-to-right text.
 pageSetup.setBidi(reverseColumns);

 doc.save(getArtifactsDir() + "PageSetup.Bidi.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getBorderAlwaysInFront() {#getBorderAlwaysInFront}
```
public boolean getBorderAlwaysInFront()
```


Sayfa kenarlığının kesişen metinler ve nesnelere göre nerede konumlandırıldığını belirtir.

 **Examples:** 

İlk sayfanın üst kısmında geniş mavi bir şerit kenarlık nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getBorderAppliesTo() {#getBorderAppliesTo}
```
public int getBorderAppliesTo()
```


Sayfa kenarlığının hangi sayfalarda basılacağını belirtir.

 **Examples:** 

İlk sayfanın üst kısmında geniş mavi bir şerit kenarlık nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/) sabitlerinden biridir.
### getBorderDistanceFrom() {#getBorderDistanceFrom}
```
public int getBorderDistanceFrom()
```


Belirtilen sayfa kenarlığının sayfanın kenarından mı yoksa çevrelediği metinden mi ölçüldüğünü gösteren bir değer alır.

 **Examples:** 

İlk sayfanın üst kısmında geniş mavi bir şerit kenarlık nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
int - Belirtilen sayfa kenarlığının sayfanın kenarından mı yoksa çevrelediği metinden mi ölçüldüğünü gösteren değer. Döndürülen değer, [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/) sabitlerinden biridir.
### getBorderSurroundsFooter() {#getBorderSurroundsFooter}
```
public boolean getBorderSurroundsFooter()
```


Sayfa kenarlığının alt bilgiyi içerip içermediğini belirtir.

 **Remarks:** 

Not: Bu özelliği değiştirmek belgedeki tüm bölümleri etkiler.

 **Examples:** 

Sayfaya ve üst bilgi/alt bilgiye kenarlık nasıl uygulanacağını gösterir.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getBorderSurroundsHeader() {#getBorderSurroundsHeader}
```
public boolean getBorderSurroundsHeader()
```


Sayfa kenarlığının üst bilgiyi içerip içermediğini belirtir.

 **Remarks:** 

Not: Bu özelliği değiştirmek belgedeki tüm bölümleri etkiler.

 **Examples:** 

Sayfaya ve üst bilgi/alt bilgiye kenarlık nasıl uygulanacağını gösterir.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Sayfa kenarlıklarının bir koleksiyonunu alır.

 **Examples:** 

Gölge ile yeşil dalgalı sayfa kenarlığı nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - A collection of the page borders.
### getBottomMargin() {#getBottomMargin}
```
public double getBottomMargin()
```


Sayfanın alt kenarı ile gövde metninin alt sınırı arasındaki mesafeyi (puan cinsinden) alır.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - Sayfanın alt kenarı ile gövde metninin alt sınırı arasındaki mesafe (nokta cinsinden).
### getChapterPageSeparator() {#getChapterPageSeparator}
```
public int getChapterPageSeparator()
```


Bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakteri alır.

 **Remarks:** 

Bölüm numaralarını içeren sayfa numaraları oluşturabilmek için, belge başlıklarının numaralı bir taslak biçimi uygulanmış olması gerekir.

 **Examples:** 

Sayfa bölümleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - Bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakter. Döndürülen değer, [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/) sabitlerinden biridir.
### getCharactersPerLine() {#getCharactersPerLine}
```
public int getCharactersPerLine()
```


Belge ızgarasındaki satır başına karakter sayısını alır.

 **Remarks:** 

Özelliğin minimum değeri 1'dir. Maksimum değer, sayfa genişliği ve Normal stilinin yazı tipi boyutuna bağlıdır. Minimum karakter aralığı, yazı tipi boyutunun yüzde 90'ıdır. Örneğin, bir inç kenar boşluklu Letter sayfasında satır başına maksimum karakter sayısı 43'tür.

Varsayılan olarak, özelliğin değeri, karakter aralığının Normal stilinin yazı tipi boyutuna eşit olduğu bir değerdir.

 **Examples:** 

Her satırın sahip olabileceği karakter sayısı için bir sınır nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

**Returns:**
int - Belge ızgarasında satır başına karakter sayısı.
### getDifferentFirstPageHeaderFooter() {#getDifferentFirstPageHeaderFooter}
```
public boolean getDifferentFirstPageHeaderFooter()
```


İlk sayfada farklı bir üst bilgi veya alt bilgi kullanılıyorsa doğru.

 **Examples:** 

DocumentBuilder kullanarak bir belgede üstbilgi ve altbilgi nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Bir metin değiştirme işleminin düğümleri hangi sırayla dolaştığını nasıl izleyebileceğinizi gösterir.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

Ana üst bilgi/alt bilgileri nasıl etkinleştireceğinizi veya devre dışı bırakacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "First" header/footer, which appears on the first page of the section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.writeln("First page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_FIRST);
 builder.writeln("First page footer.");

 // 2 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
 // Set the "DifferentFirstPageHeaderFooter" property to "false"
 // to make the first page display the primary header/footer.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.DifferentFirstPageHeaderFooter.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
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
### getEndnoteOptions() {#getEndnoteOptions}
```
public EndnoteOptions getEndnoteOptions()
```


Bu bölümde dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sunar.

 **Examples:** 

Bir bölümde dipnotları/sonnotları etkileyen seçenekleri nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote reference text.");

 // Configure all footnotes in the first section to restart the numbering from 1
 // at each new page and display themselves directly beneath the text on every page.
 FootnoteOptions footnoteOptions = doc.getSections().get(0).getPageSetup().getFootnoteOptions();
 footnoteOptions.setPosition(FootnotePosition.BENEATH_TEXT);
 footnoteOptions.setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 footnoteOptions.setStartNumber(1);

 builder.write(" Hello again.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Endnote reference text.");

 // Configure all endnotes in the first section to maintain a continuous count throughout the section,
 // starting from 1. Also, set them all to appear collected at the end of the document.
 EndnoteOptions endnoteOptions = doc.getSections().get(0).getPageSetup().getEndnoteOptions();
 endnoteOptions.setPosition(EndnotePosition.END_OF_DOCUMENT);
 endnoteOptions.setRestartRule(FootnoteNumberingRule.CONTINUOUS);
 endnoteOptions.setStartNumber(1);

 doc.save(getArtifactsDir() + "PageSetup.FootnoteOptions.docx");
 
```

**Returns:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions/) - The corresponding [EndnoteOptions](../../com.aspose.words/endnoteoptions/) value.
### getFirstPageTray() {#getFirstPageTray}
```
public int getFirstPageTray()
```


Bir bölümün ilk sayfası için kullanılacak kağıt tepsisini (bin) alır. Değer, uygulamaya (yazıcıya) özgüdür.

 **Examples:** 

Farklı kağıt boyutları için farklı yazıcı tepsileri kullanarak yazdırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Returns:**
int - Bir bölümün ilk sayfası için kullanılacak kağıt tepsisi (bin).
### getFooterDistance() {#getFooterDistance}
```
public double getFooterDistance()
```


Alt bilgi ile sayfanın alt kısmı arasındaki mesafeyi (puan cinsinden) alır.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - Alt bilgi ile sayfanın alt kısmı arasındaki mesafe (nokta cinsinden).
### getFootnoteOptions() {#getFootnoteOptions}
```
public FootnoteOptions getFootnoteOptions()
```


Bu bölümde altnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sunar.

 **Examples:** 

Bir bölümde dipnotları/sonnotları etkileyen seçenekleri nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote reference text.");

 // Configure all footnotes in the first section to restart the numbering from 1
 // at each new page and display themselves directly beneath the text on every page.
 FootnoteOptions footnoteOptions = doc.getSections().get(0).getPageSetup().getFootnoteOptions();
 footnoteOptions.setPosition(FootnotePosition.BENEATH_TEXT);
 footnoteOptions.setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 footnoteOptions.setStartNumber(1);

 builder.write(" Hello again.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Endnote reference text.");

 // Configure all endnotes in the first section to maintain a continuous count throughout the section,
 // starting from 1. Also, set them all to appear collected at the end of the document.
 EndnoteOptions endnoteOptions = doc.getSections().get(0).getPageSetup().getEndnoteOptions();
 endnoteOptions.setPosition(EndnotePosition.END_OF_DOCUMENT);
 endnoteOptions.setRestartRule(FootnoteNumberingRule.CONTINUOUS);
 endnoteOptions.setStartNumber(1);

 doc.save(getArtifactsDir() + "PageSetup.FootnoteOptions.docx");
 
```

**Returns:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions/) - The corresponding [FootnoteOptions](../../com.aspose.words/footnoteoptions/) value.
### getGutter() {#getGutter}
```
public double getGutter()
```


Belge ciltleme için kenarlığa eklenen ekstra boşluk miktarını alır.

 **Examples:** 

Kanal kenar boşluklarını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
double - Belge ciltlemesi için kenara eklenen ekstra boşluk miktarı.
### getHeaderDistance() {#getHeaderDistance}
```
public double getHeaderDistance()
```


Üst bilgi ile sayfanın üst kısmı arasındaki mesafeyi (puan cinsinden) alır.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - Üstbilgi ile sayfanın üst kenarı arasındaki (puan cinsinden) mesafe.
### getHeadingLevelForChapter() {#getHeadingLevelForChapter}
```
public int getHeadingLevelForChapter()
```


Belgedeki bölüm başlıklarına uygulanan başlık düzeyi stilini alır.

 **Remarks:** 

0 ile 9 arasında bir sayı olabilir. 0, sayfa numarasına uygulandığında bölüm numarası olmadığını ifade eder.

Bölüm numaralarını içeren sayfa numaraları oluşturabilmek için, belge başlıklarının numaralı bir taslak biçimi uygulanmış olması gerekir.

 **Examples:** 

Sayfa bölümleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - Belgede bölüm başlıklarına uygulanan başlık seviyesi stili.
### getLayoutMode() {#getLayoutMode}
```
public int getLayoutMode()
```


Bu bölümün düzen modunu alır.

 **Examples:** 

Her satırın sahip olabileceği karakter sayısı için bir sınır nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Her sayfanın sahip olabileceği satır sayısı için bir sınırın nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
int - Bu bölümün yerleşim modu. Döndürülen değer, [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/) sabitlerinden biridir.
### getLeftMargin() {#getLeftMargin}
```
public double getLeftMargin()
```


Sayfanın sol kenarı ile gövde metninin sol sınırı arasındaki mesafeyi (puan cinsinden) alır.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - Sayfanın sol kenarı ile gövde metninin sol sınırı arasındaki (puan cinsinden) mesafe.
### getLineNumberCountBy() {#getLineNumberCountBy}
```
public int getLineNumberCountBy()
```


Satır numaraları için sayısal artışı alır.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - Satır numaraları için sayısal artış.
### getLineNumberDistanceFromText() {#getLineNumberDistanceFromText}
```
public double getLineNumberDistanceFromText()
```


Satır numaralarının sağ kenarı ile belgenin sol kenarı arasındaki mesafeyi alır.

 **Remarks:** 

Satır numaraları ile belgenin metni arasındaki otomatik mesafe için bu özelliği sıfıra ayarlayın.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
double - Satır numaralarının sağ kenarı ile belgenin sol kenarı arasındaki mesafe.
### getLineNumberRestartMode() {#getLineNumberRestartMode}
```
public int getLineNumberRestartMode()
```


Satır numaralandırmasının nasıl çalıştığını alır; yani yeni bir sayfa veya bölümün başında yeniden başlayıp başlamadığını veya sürekli devam edip etmediğini.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - Satır numaralandırmanın nasıl çalıştığı; yeni bir sayfa veya bölümün başında yeniden başlayıp ya da sürekli devam edip etmediği. Döndürülen değer, [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/) sabitlerinden biridir.
### getLineStartingNumber() {#getLineStartingNumber}
```
public int getLineStartingNumber()
```


Başlangıç satır numarasını alır.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - Başlangıç satır numarası.
### getLinesPerPage() {#getLinesPerPage}
```
public int getLinesPerPage()
```


Belge ızgarasındaki sayfa başına satır sayısını alır.

 **Remarks:** 

Özelliğin minimum değeri 1'dir. Maksimum değer, sayfa yüksekliği ve Normal stilinin yazı tipi boyutuna bağlıdır. Minimum satır aralığı, yazı tipi boyutunun %136'sıdır. Örneğin, bir inç kenar boşluklu Letter sayfasında sayfa başına maksimum satır sayısı 39'dur.

Varsayılan olarak, özelliğin değeri, satır aralığının Normal stilinin yazı tipi boyutundan 1,5 kat daha büyük olduğu bir değerdir.

 **Examples:** 

Her sayfanın sahip olabileceği satır sayısı için bir sınırın nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
int - Belge ızgarasındaki sayfa başına satır sayısı.
### getMargins() {#getMargins}
```
public int getMargins()
```


Sayfanın önceden ayarlanmış [Margins](../../com.aspose.words/margins/) değerini alır.

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

**Returns:**
int - Sayfanın önceden ayarlanmış [Margins](../../com.aspose.words/margins/) değerleri. Döndürülen değer, [Margins](../../com.aspose.words/margins/) sabitlerinden biridir.
### getMultiplePages() {#getMultiplePages}
```
public int getMultiplePages()
```


Birden çok sayfalı belgeler için, belgenin bir kitapçık olarak ciltlenebilmesi için nasıl yazdırıldığını veya oluşturulduğunu alır veya ayarlar.

 **Examples:** 

Kanal kenar boşluklarını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [MultiplePagesType](../../com.aspose.words/multiplepagestype/) sabitlerinden biridir.
### getOddAndEvenPagesHeaderFooter() {#getOddAndEvenPagesHeaderFooter}
```
public boolean getOddAndEvenPagesHeaderFooter()
```


Belgenin tek sayfalar ve çift sayfalar için farklı üstbilgi ve altbilgi içeriyorsa True.

 **Remarks:** 

Not: Bu özelliği değiştirmek belgedeki tüm bölümleri etkiler.

 **Examples:** 

DocumentBuilder kullanarak bir belgede üstbilgi ve altbilgi nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Çift sayfa üstbilgi/altbilgilerini nasıl etkinleştireceğinizi veya devre dışı bırakacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 // 2 -  The "Even" header/footer, which appears on every even page of this section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.writeln("Even page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_EVEN);
 builder.writeln("Even page footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "OddAndEvenPagesHeaderFooter" property to "true"
 // to display the even page header/footer on even pages.
 // Set the "OddAndEvenPagesHeaderFooter" property to "false"
 // to display the primary header/footer on even pages.
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Sayfanın yönünü alır.

 **Remarks:** 

Değiştirilen [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int), [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) ve [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double) değerlerinin yerini değiştirir.

 **Examples:** 

Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma işlemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
int - Sayfanın yönü. Döndürülen değer, [Orientation](../../com.aspose.words/orientation/) sabitlerinden biridir.
### getOtherPagesTray() {#getOtherPagesTray}
```
public int getOtherPagesTray()
```


Bir bölümün ilk sayfası dışındaki tüm sayfalar için kullanılacak kağıt tepsisini (bin) alır. Değer, uygulamaya (yazıcıya) özgüdür.

 **Examples:** 

Farklı kağıt boyutları için farklı yazıcı tepsileri kullanarak yazdırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Returns:**
int - Bir bölümün ilk sayfası dışındaki tüm sayfalar için kullanılacak kağıt tepsisi (bin).
### getPageHeight() {#getPageHeight}
```
public double getPageHeight()
```


Sayfanın yüksekliğini puan cinsinden alır.

 **Examples:** 

Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

**Returns:**
double - Sayfanın yüksekliği (nokta cinsinden).
### getPageNumberStyle() {#getPageNumberStyle}
```
public int getPageNumberStyle()
```


Sayfa numarası biçimini alır.

 **Examples:** 

Bir bölümde sayfa numaralandırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
int - Sayfa numarası biçimi. Döndürülen değer, [NumberStyle](../../com.aspose.words/numberstyle/) sabitlerinden biridir.
### getPageStartingNumber() {#getPageStartingNumber}
```
public int getPageStartingNumber()
```


Bölümün başlangıç sayfa numarasını alır.

 **Remarks:** 

Bu [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) özelliği, false olarak ayarlanırsa, [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) özelliğini geçersiz kılar ve sayfa numaralandırması önceki bölümden devam edebilir.

 **Examples:** 

Bir bölümde sayfa numaralandırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
int - Bölümün başlangıç sayfa numarası.
### getPageWidth() {#getPageWidth}
```
public double getPageWidth()
```


Sayfanın genişliğini puan cinsinden alır.

 **Examples:** 

Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Yüzen bir görüntünün nasıl ekleneceğini ve konumunun ve boyutunun nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
double - Sayfanın genişliği (nokta cinsinden).
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Kağıt boyutunu alır.

 **Remarks:** 

Bu özelliği ayarlamak, [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) ve [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double) değerlerini günceller. Bu değeri [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) olarak ayarlamak mevcut değerleri değiştirmez.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Sayfa boyutlarının nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can change the current page's size to a pre-defined size
 // by using the "PaperSize" property of this section's PageSetup object.
 builder.getPageSetup().setPaperSize(PaperSize.TABLOID);

 Assert.assertEquals(792.0d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(1224.0d, builder.getPageSetup().getPageHeight());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 // Each section has its own PageSetup object. When we use a document builder to make a new section,
 // that section's PageSetup object inherits all the previous section's PageSetup object's values.
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 Assert.assertEquals(PaperSize.TABLOID, builder.getPageSetup().getPaperSize());

 builder.getPageSetup().setPaperSize(PaperSize.A5);
 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 Assert.assertEquals(419.55d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(595.30d, builder.getPageSetup().getPageHeight());

 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 // Set a custom size for this section's pages.
 builder.getPageSetup().setPageWidth(620.0);
 builder.getPageSetup().setPageHeight(480.0);

 Assert.assertEquals(PaperSize.CUSTOM, builder.getPageSetup().getPaperSize());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 doc.save(getArtifactsDir() + "PageSetup.PaperSizes.docx");
 
```

JisB4 veya JisB5 kağıt boyutunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
int - Kağıt boyutu. Döndürülen değer, [PaperSize](../../com.aspose.words/papersize/) sabitlerinden biridir.
### getRestartPageNumbering() {#getRestartPageNumbering}
```
public boolean getRestartPageNumbering()
```


Sayfa numaralandırması bölümün başında yeniden başlıyorsa True.

 **Remarks:** 

false olarak ayarlanırsa, [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) özelliği, [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) özelliğini geçersiz kılar ve sayfa numaralandırması önceki bölümden devam edebilir.

 **Examples:** 

Bir bölümde sayfa numaralandırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getRightMargin() {#getRightMargin}
```
public double getRightMargin()
```


Sayfanın sağ kenarı ile metin gövdesinin sağ sınırı arasındaki mesafeyi (puan cinsinden) alır.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - Sayfanın sağ kenarı ile gövde metninin sağ sınırı arasındaki mesafe (nokta cinsinden).
### getRtlGutter() {#getRtlGutter}
```
public boolean getRtlGutter()
```


Microsoft Word'ün bölümü sağdan sola veya soldan sağa dillerine göre oluk (gutter) kullanıp kullanmadığını alır.

 **Examples:** 

Kanal kenar boşluklarını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

**Returns:**
boolean - Microsoft Word'ün, sağdan sola veya soldan sağa dillerine göre bölüm için olukları kullanıp kullanmadığını belirtir.
### getSectionStart() {#getSectionStart}
```
public int getSectionStart()
```


Belirtilen nesne için bölüm sonu tipini alır.

 **Examples:** 

Yeni bir bölümün önceki bölüme nasıl ayrıldığını belirtmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
int - Belirtilen nesne için bölüm sonu tipi. Döndürülen değer, [SectionStart](../../com.aspose.words/sectionstart/) sabitlerinden biridir.
### getSheetsPerBooklet() {#getSheetsPerBooklet}
```
public int getSheetsPerBooklet()
```


Her kitapçıkta bulunacak sayfa sayısını alır.

 **Examples:** 

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
int - Her kitapçıkta yer alacak sayfa sayısı.
### getSuppressEndnotes() {#getSuppressEndnotes}
```
public boolean getSuppressEndnotes()
```


True if endnotlar, endnotları bastırmayan bir sonraki bölümün sonunda yazdırılıyorsa. Bastırılan endnotlar, o bölümdeki endnotların önünde yazdırılır.

 **Examples:** 

Endnotların her bölümün sonunda nasıl saklanacağını ve konumlarının nasıl değiştirileceğini gösterir.

```

 public void suppressEndnotes() throws Exception {
     Document doc = new Document();
     doc.removeAllChildren();

     // By default, a document compiles all endnotes at its end.
     Assert.assertEquals(EndnotePosition.END_OF_DOCUMENT, doc.getEndnoteOptions().getPosition());

     // We use the "Position" property of the document's "EndnoteOptions" object
     // to collect endnotes at the end of each section instead.
     doc.getEndnoteOptions().setPosition(EndnotePosition.END_OF_SECTION);

     insertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
     insertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
     insertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

     // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
     // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
     // onto the next section.
     PageSetup pageSetup = doc.getSections().get(1).getPageSetup();
     pageSetup.setSuppressEndnotes(true);

     doc.save(getArtifactsDir() + "PageSetup.SuppressEndnotes.docx");
 }

 /// 
 /// Append a section with text and an endnote to a document.
 /// 
 private static void insertSectionWithEndnote(Document doc, String sectionBodyText, String endnoteText) {
     Section section = new Section(doc);

     doc.appendChild(section);

     Body body = new Body(doc);
     section.appendChild(body);

     Assert.assertEquals(body.getParentNode(), section);

     Paragraph para = new Paragraph(doc);
     body.appendChild(para);

     Assert.assertEquals(para.getParentNode(), body);

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.moveTo(para);
     builder.write(sectionBodyText);
     builder.insertFootnote(FootnoteType.ENDNOTE, endnoteText);
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getTextColumns() {#getTextColumns}
```
public TextColumnCollection getTextColumns()
```


Metin sütunları kümesini temsil eden bir koleksiyon döndürür.

 **Examples:** 

Bir bölümde birden fazla eşit aralıklı sütun oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
[TextColumnCollection](../../com.aspose.words/textcolumncollection/) - A collection that represents the set of text columns.
### getTextOrientation() {#getTextOrientation}
```
public int getTextOrientation()
```


Tüm sayfa için [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) belirtmeye olanak tanır. Varsayılan değer [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL).

 **Remarks:** 

Bu özellik yalnızca MS Word yerel formatları DOCX, WML, RTF ve DOC için desteklenir.

 **Examples:** 

Metin yönünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
 // to the right so that all left-to-right text now goes top-to-bottom.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTextOrientation(TextOrientation.UPWARD);

 doc.save(getArtifactsDir() + "PageSetup.SetTextOrientation.docx");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [TextOrientation](../../com.aspose.words/textorientation/) sabitlerinden biridir.
### getTopMargin() {#getTopMargin}
```
public double getTopMargin()
```


Sayfanın üst kenarı ile metin gövdesinin üst sınırı arasındaki mesafeyi (puan cinsinden) alır.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - Sayfanın üst kenarı ile gövde metninin üst sınırı arasındaki mesafe (nokta cinsinden).
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Bir belge veya bölümdeki her sayfadaki metnin dikey hizalamasını alır.

 **Examples:** 

Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma işlemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
int - Bir belge veya bölümdeki her sayfadaki metnin dikey hizalaması. Döndürülen değer, [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/) sabitlerinden biridir.
### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Bu bölümün çift yönlü (karmaşık betikler) metin içerdiğini belirtir.

 **Remarks:** 

Doğru olduğunda, bu bölmedeki sütunlar sağdan sola yerleştirilir.

 **Examples:** 

Bir bölümdeki metin sütunlarının sırasını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getTextColumns().setCount(3);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 3.");

 // Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
 // The order of the columns will match the direction of the right-to-left text.
 // Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
 // The order of the columns will match the direction of the left-to-right text.
 pageSetup.setBidi(reverseColumns);

 doc.save(getArtifactsDir() + "PageSetup.Bidi.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBorderAlwaysInFront(boolean value) {#setBorderAlwaysInFront-boolean}
```
public void setBorderAlwaysInFront(boolean value)
```


Sayfa kenarlığının kesişen metinler ve nesnelere göre nerede konumlandırıldığını belirtir.

 **Examples:** 

İlk sayfanın üst kısmında geniş mavi bir şerit kenarlık nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBorderAppliesTo(int value) {#setBorderAppliesTo-int}
```
public void setBorderAppliesTo(int value)
```


Sayfa kenarlığının hangi sayfalarda basılacağını belirtir.

 **Examples:** 

İlk sayfanın üst kısmında geniş mavi bir şerit kenarlık nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/) sabitlerinden biri olmalıdır. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setBorderDistanceFrom(int value) {#setBorderDistanceFrom-int}
```
public void setBorderDistanceFrom(int value)
```


Belirtilen sayfa kenarlığının sayfanın kenarından mı yoksa çevresindeki metinden mi ölçüldüğünü gösteren bir değeri ayarlar.

 **Examples:** 

İlk sayfanın üst kısmında geniş mavi bir şerit kenarlık nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Belirtilen sayfa kenarlığının sayfanın kenarından mı yoksa çevrelediği metinden mi ölçüldüğünü gösteren bir değer. Değer, [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/) sabitlerinden biri olmalıdır. |

### setBorderSurroundsFooter(boolean value) {#setBorderSurroundsFooter-boolean}
```
public void setBorderSurroundsFooter(boolean value)
```


Sayfa kenarlığının alt bilgiyi içerip içermediğini belirtir.

 **Remarks:** 

Not: Bu özelliği değiştirmek belgedeki tüm bölümleri etkiler.

 **Examples:** 

Sayfaya ve üst bilgi/alt bilgiye kenarlık nasıl uygulanacağını gösterir.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBorderSurroundsHeader(boolean value) {#setBorderSurroundsHeader-boolean}
```
public void setBorderSurroundsHeader(boolean value)
```


Sayfa kenarlığının üst bilgiyi içerip içermediğini belirtir.

 **Remarks:** 

Not: Bu özelliği değiştirmek belgedeki tüm bölümleri etkiler.

 **Examples:** 

Sayfaya ve üst bilgi/alt bilgiye kenarlık nasıl uygulanacağını gösterir.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBottomMargin(double value) {#setBottomMargin-double}
```
public void setBottomMargin(double value)
```


Sayfanın alt kenarı ile gövde metninin alt sınırı arasındaki mesafeyi (nokta cinsinden) ayarlar.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Sayfanın alt kenarı ile gövde metninin alt sınırı arasındaki (nokta cinsinden) mesafe. |

### setChapterPageSeparator(int value) {#setChapterPageSeparator-int}
```
public void setChapterPageSeparator(int value)
```


Bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakteri ayarlar.

 **Remarks:** 

Bölüm numaralarını içeren sayfa numaraları oluşturabilmek için, belge başlıklarının numaralı bir taslak biçimi uygulanmış olması gerekir.

 **Examples:** 

Sayfa bölümleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakter. Değer, [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/) sabitlerinden biri olmalıdır. |

### setCharactersPerLine(int value) {#setCharactersPerLine-int}
```
public void setCharactersPerLine(int value)
```


Belge ızgarasındaki satır başına karakter sayısını ayarlar.

 **Remarks:** 

Özelliğin minimum değeri 1'dir. Maksimum değer, sayfa genişliği ve Normal stilinin yazı tipi boyutuna bağlıdır. Minimum karakter aralığı, yazı tipi boyutunun yüzde 90'ıdır. Örneğin, bir inç kenar boşluklu Letter sayfasında satır başına maksimum karakter sayısı 43'tür.

Varsayılan olarak, özelliğin değeri, karakter aralığının Normal stilinin yazı tipi boyutuna eşit olduğu bir değerdir.

 **Examples:** 

Her satırın sahip olabileceği karakter sayısı için bir sınır nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Belge ızgarasındaki satır başına karakter sayısı. |

### setDifferentFirstPageHeaderFooter(boolean value) {#setDifferentFirstPageHeaderFooter-boolean}
```
public void setDifferentFirstPageHeaderFooter(boolean value)
```


İlk sayfada farklı bir üst bilgi veya alt bilgi kullanılıyorsa doğru.

 **Examples:** 

DocumentBuilder kullanarak bir belgede üstbilgi ve altbilgi nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Bir metin değiştirme işleminin düğümleri hangi sırayla dolaştığını nasıl izleyebileceğinizi gösterir.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

Ana üst bilgi/alt bilgileri nasıl etkinleştireceğinizi veya devre dışı bırakacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "First" header/footer, which appears on the first page of the section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.writeln("First page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_FIRST);
 builder.writeln("First page footer.");

 // 2 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
 // Set the "DifferentFirstPageHeaderFooter" property to "false"
 // to make the first page display the primary header/footer.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.DifferentFirstPageHeaderFooter.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setFirstPageTray(int value) {#setFirstPageTray-int}
```
public void setFirstPageTray(int value)
```


Bir bölümün ilk sayfası için kullanılacak kağıt tepsisini (bin) ayarlar. Değer, uygulamaya (yazıcıya) özgüdür.

 **Examples:** 

Farklı kağıt boyutları için farklı yazıcı tepsileri kullanarak yazdırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Bir bölümün ilk sayfası için kullanılacak kağıt tepsisi (bin). |

### setFooterDistance(double value) {#setFooterDistance-double}
```
public void setFooterDistance(double value)
```


Altbilgi ile sayfanın alt kısmı arasındaki mesafeyi (nokta cinsinden) ayarlar.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Alt bilgi ile sayfanın alt kısmı arasındaki (nokta cinsinden) mesafe. |

### setGutter(double value) {#setGutter-double}
```
public void setGutter(double value)
```


Belge ciltleme için kenara eklenen ekstra boşluk miktarını ayarlar.

 **Examples:** 

Kanal kenar boşluklarını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Belge ciltlemesi için kenara eklenen ekstra boşluk miktarı. |

### setHeaderDistance(double value) {#setHeaderDistance-double}
```
public void setHeaderDistance(double value)
```


Üstbilgi ile sayfanın üst kısmı arasındaki mesafeyi (nokta cinsinden) ayarlar.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Üst bilgi ile sayfanın üst kısmı arasındaki (nokta cinsinden) mesafe. |

### setHeadingLevelForChapter(int value) {#setHeadingLevelForChapter-int}
```
public void setHeadingLevelForChapter(int value)
```


Belgedeki bölüm başlıklarına uygulanan başlık seviyesi stilini ayarlar.

 **Remarks:** 

0 ile 9 arasında bir sayı olabilir. 0, sayfa numarasına uygulandığında bölüm numarası olmadığını ifade eder.

Bölüm numaralarını içeren sayfa numaraları oluşturabilmek için, belge başlıklarının numaralı bir taslak biçimi uygulanmış olması gerekir.

 **Examples:** 

Sayfa bölümleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Belgedeki bölüm başlıklarına uygulanan başlık seviyesi stili. |

### setLayoutMode(int value) {#setLayoutMode-int}
```
public void setLayoutMode(int value)
```


Bu bölümün yerleşim modunu ayarlar.

 **Examples:** 

Her satırın sahip olabileceği karakter sayısı için bir sınır nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Her sayfanın sahip olabileceği satır sayısı için bir sınırın nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu bölümün yerleşim modu. Değer, [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/) sabitlerinden biri olmalıdır. |

### setLeftMargin(double value) {#setLeftMargin-double}
```
public void setLeftMargin(double value)
```


Sayfanın sol kenarı ile gövde metninin sol sınırı arasındaki mesafeyi (nokta cinsinden) ayarlar.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Sayfanın sol kenarı ile gövde metninin sol sınırı arasındaki (nokta cinsinden) mesafe. |

### setLineNumberCountBy(int value) {#setLineNumberCountBy-int}
```
public void setLineNumberCountBy(int value)
```


Satır numaraları için sayısal artışı ayarlar.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Satır numaraları için sayısal artış. |

### setLineNumberDistanceFromText(double value) {#setLineNumberDistanceFromText-double}
```
public void setLineNumberDistanceFromText(double value)
```


Satır numaralarının sağ kenarı ile belgenin sol kenarı arasındaki mesafeyi ayarlar.

 **Remarks:** 

Satır numaraları ile belgenin metni arasındaki otomatik mesafe için bu özelliği sıfıra ayarlayın.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Satır numaralarının sağ kenarı ile belgenin sol kenarı arasındaki mesafe. |

### setLineNumberRestartMode(int value) {#setLineNumberRestartMode-int}
```
public void setLineNumberRestartMode(int value)
```


Satır numaralandırmasının nasıl çalışacağını ayarlar; yani yeni bir sayfa ya da bölümün başında yeniden başlayıp başlamayacağını ya da sürekli devam edip etmeyeceğini belirler.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Satır numaralandırmasının nasıl çalıştığı; yani yeni bir sayfa ya da bölümün başında yeniden başlayıp başlamadığı ya da sürekli devam edip etmediği. Değer, [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/) sabitlerinden biri olmalıdır. |

### setLineStartingNumber(int value) {#setLineStartingNumber-int}
```
public void setLineStartingNumber(int value)
```


Başlangıç satır numarasını ayarlar.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Başlangıç satır numarası. |

### setLinesPerPage(int value) {#setLinesPerPage-int}
```
public void setLinesPerPage(int value)
```


Belge ızgarasındaki sayfa başına satır sayısını ayarlar.

 **Remarks:** 

Özelliğin minimum değeri 1'dir. Maksimum değer, sayfa yüksekliği ve Normal stilinin yazı tipi boyutuna bağlıdır. Minimum satır aralığı, yazı tipi boyutunun %136'sıdır. Örneğin, bir inç kenar boşluklu Letter sayfasında sayfa başına maksimum satır sayısı 39'dur.

Varsayılan olarak, özelliğin değeri, satır aralığının Normal stilinin yazı tipi boyutundan 1,5 kat daha büyük olduğu bir değerdir.

 **Examples:** 

Her sayfanın sahip olabileceği satır sayısı için bir sınırın nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Belge ızgarasındaki sayfa başına satır sayısı. |

### setMargins(int value) {#setMargins-int}
```
public void setMargins(int value)
```


Sayfanın önceden ayarlanmış [Margins](../../com.aspose.words/margins/) ayarlarını belirler.

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
| value | int | Sayfanın önceden ayarlanmış [Margins](../../com.aspose.words/margins/) değerleri. Değer, [Margins](../../com.aspose.words/margins/) sabitlerinden biri olmalıdır. |

### setMultiplePages(int value) {#setMultiplePages-int}
```
public void setMultiplePages(int value)
```


Birden çok sayfalı belgeler için, belgenin bir kitapçık olarak ciltlenebilmesi için nasıl yazdırıldığını veya oluşturulduğunu alır veya ayarlar.

 **Examples:** 

Kanal kenar boşluklarını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [MultiplePagesType](../../com.aspose.words/multiplepagestype/) sabitlerinden biri olmalıdır. |

### setOddAndEvenPagesHeaderFooter(boolean value) {#setOddAndEvenPagesHeaderFooter-boolean}
```
public void setOddAndEvenPagesHeaderFooter(boolean value)
```


Belgenin tek sayfalar ve çift sayfalar için farklı üstbilgi ve altbilgi içeriyorsa True.

 **Remarks:** 

Not: Bu özelliği değiştirmek belgedeki tüm bölümleri etkiler.

 **Examples:** 

DocumentBuilder kullanarak bir belgede üstbilgi ve altbilgi nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Çift sayfa üstbilgi/altbilgilerini nasıl etkinleştireceğinizi veya devre dışı bırakacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 // 2 -  The "Even" header/footer, which appears on every even page of this section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.writeln("Even page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_EVEN);
 builder.writeln("Even page footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "OddAndEvenPagesHeaderFooter" property to "true"
 // to display the even page header/footer on even pages.
 // Set the "OddAndEvenPagesHeaderFooter" property to "false"
 // to display the primary header/footer on even pages.
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Sayfanın yönlendirmesini ayarlar.

 **Remarks:** 

Değiştirilen [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int), [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) ve [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double) değerlerinin yerini değiştirir.

 **Examples:** 

Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma işlemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Sayfanın yönü. Değer, [Orientation](../../com.aspose.words/orientation/) sabitlerinden biri olmalıdır. |

### setOtherPagesTray(int value) {#setOtherPagesTray-int}
```
public void setOtherPagesTray(int value)
```


Bir bölümün ilk sayfası dışındaki tüm sayfalar için kullanılacak kağıt tepsisini (bin) ayarlar. Değer, uygulamaya (yazıcıya) özgüdür.

 **Examples:** 

Farklı kağıt boyutları için farklı yazıcı tepsileri kullanarak yazdırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Bir bölümün ilk sayfası dışındaki tüm sayfalar için kullanılacak kağıt tepsisi (bin). |

### setPageHeight(double value) {#setPageHeight-double}
```
public void setPageHeight(double value)
```


Sayfanın yüksekliğini nokta cinsinden ayarlar.

 **Examples:** 

Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Sayfanın nokta cinsinden yüksekliği. |

### setPageNumberStyle(int value) {#setPageNumberStyle-int}
```
public void setPageNumberStyle(int value)
```


Sayfa numarası biçimini ayarlar.

 **Examples:** 

Bir bölümde sayfa numaralandırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Sayfa numarası biçimi. Değer, [NumberStyle](../../com.aspose.words/numberstyle/) sabitlerinden biri olmalıdır. |

### setPageStartingNumber(int value) {#setPageStartingNumber-int}
```
public void setPageStartingNumber(int value)
```


Bölümün başlangıç sayfa numarasını ayarlar.

 **Remarks:** 

Bu [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) özelliği, false olarak ayarlanırsa, [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) özelliğini geçersiz kılar ve sayfa numaralandırması önceki bölümden devam edebilir.

 **Examples:** 

Bir bölümde sayfa numaralandırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Bölümün başlangıç sayfa numarası. |

### setPageWidth(double value) {#setPageWidth-double}
```
public void setPageWidth(double value)
```


Sayfanın genişliğini nokta cinsinden ayarlar.

 **Examples:** 

Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Yüzen bir görüntünün nasıl ekleneceğini ve konumunun ve boyutunun nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Sayfanın genişliği puan cinsinden. |

### setPaperSize(int value) {#setPaperSize-int}
```
public void setPaperSize(int value)
```


Kağıt boyutunu ayarlar.

 **Remarks:** 

Bu özelliği ayarlamak, [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) ve [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double) değerlerini günceller. Bu değeri [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) olarak ayarlamak mevcut değerleri değiştirmez.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Sayfa boyutlarının nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can change the current page's size to a pre-defined size
 // by using the "PaperSize" property of this section's PageSetup object.
 builder.getPageSetup().setPaperSize(PaperSize.TABLOID);

 Assert.assertEquals(792.0d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(1224.0d, builder.getPageSetup().getPageHeight());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 // Each section has its own PageSetup object. When we use a document builder to make a new section,
 // that section's PageSetup object inherits all the previous section's PageSetup object's values.
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 Assert.assertEquals(PaperSize.TABLOID, builder.getPageSetup().getPaperSize());

 builder.getPageSetup().setPaperSize(PaperSize.A5);
 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 Assert.assertEquals(419.55d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(595.30d, builder.getPageSetup().getPageHeight());

 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 // Set a custom size for this section's pages.
 builder.getPageSetup().setPageWidth(620.0);
 builder.getPageSetup().setPageHeight(480.0);

 Assert.assertEquals(PaperSize.CUSTOM, builder.getPageSetup().getPaperSize());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 doc.save(getArtifactsDir() + "PageSetup.PaperSizes.docx");
 
```

JisB4 veya JisB5 kağıt boyutunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Kağıt boyutu. Değer, [PaperSize](../../com.aspose.words/papersize/) sabitlerinden biri olmalıdır. |

### setRestartPageNumbering(boolean value) {#setRestartPageNumbering-boolean}
```
public void setRestartPageNumbering(boolean value)
```


Sayfa numaralandırması bölümün başında yeniden başlıyorsa True.

 **Remarks:** 

false olarak ayarlanırsa, [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) özelliği, [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) özelliğini geçersiz kılar ve sayfa numaralandırması önceki bölümden devam edebilir.

 **Examples:** 

Bir bölümde sayfa numaralandırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setRightMargin(double value) {#setRightMargin-double}
```
public void setRightMargin(double value)
```


Sayfanın sağ kenarı ile gövde metninin sağ sınırı arasındaki mesafeyi (nokta cinsinden) ayarlar.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Sayfanın sağ kenarı ile gövde metnin sağ sınırı arasındaki mesafe (puan cinsinden). |

### setRtlGutter(boolean value) {#setRtlGutter-boolean}
```
public void setRtlGutter(boolean value)
```


Microsoft Word'ün bölüme, sağdan sola ya da soldan sağa dillerine göre oluk (gutter) kullanıp kullanmayacağını ayarlar.

 **Examples:** 

Kanal kenar boşluklarını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Microsoft Word'ün bölümü sağdan sola veya soldan sağa diline göre olukları kullanıp kullanmayacağı. |

### setSectionStart(int value) {#setSectionStart-int}
```
public void setSectionStart(int value)
```


Belirtilen nesne için bölüm sonu tipini ayarlar.

 **Examples:** 

Yeni bir bölümün önceki bölüme nasıl ayrıldığını belirtmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Belirtilen nesne için bölüm sonu türü. Değer, [SectionStart](../../com.aspose.words/sectionstart/) sabitlerinden biri olmalıdır. |

### setSheetsPerBooklet(int value) {#setSheetsPerBooklet-int}
```
public void setSheetsPerBooklet(int value)
```


Her kitapçıkta dahil edilecek sayfa sayısını ayarlar.

 **Examples:** 

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Her kitapçıkta dahil edilecek sayfa sayısı. |

### setSuppressEndnotes(boolean value) {#setSuppressEndnotes-boolean}
```
public void setSuppressEndnotes(boolean value)
```


True if endnotlar, endnotları bastırmayan bir sonraki bölümün sonunda yazdırılıyorsa. Bastırılan endnotlar, o bölümdeki endnotların önünde yazdırılır.

 **Examples:** 

Endnotların her bölümün sonunda nasıl saklanacağını ve konumlarının nasıl değiştirileceğini gösterir.

```

 public void suppressEndnotes() throws Exception {
     Document doc = new Document();
     doc.removeAllChildren();

     // By default, a document compiles all endnotes at its end.
     Assert.assertEquals(EndnotePosition.END_OF_DOCUMENT, doc.getEndnoteOptions().getPosition());

     // We use the "Position" property of the document's "EndnoteOptions" object
     // to collect endnotes at the end of each section instead.
     doc.getEndnoteOptions().setPosition(EndnotePosition.END_OF_SECTION);

     insertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
     insertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
     insertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

     // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
     // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
     // onto the next section.
     PageSetup pageSetup = doc.getSections().get(1).getPageSetup();
     pageSetup.setSuppressEndnotes(true);

     doc.save(getArtifactsDir() + "PageSetup.SuppressEndnotes.docx");
 }

 /// 
 /// Append a section with text and an endnote to a document.
 /// 
 private static void insertSectionWithEndnote(Document doc, String sectionBodyText, String endnoteText) {
     Section section = new Section(doc);

     doc.appendChild(section);

     Body body = new Body(doc);
     section.appendChild(body);

     Assert.assertEquals(body.getParentNode(), section);

     Paragraph para = new Paragraph(doc);
     body.appendChild(para);

     Assert.assertEquals(para.getParentNode(), body);

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.moveTo(para);
     builder.write(sectionBodyText);
     builder.insertFootnote(FootnoteType.ENDNOTE, endnoteText);
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setTextOrientation(int value) {#setTextOrientation-int}
```
public void setTextOrientation(int value)
```


Tüm sayfa için [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) belirtmeye olanak tanır. Varsayılan değer [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL).

 **Remarks:** 

Bu özellik yalnızca MS Word yerel formatları DOCX, WML, RTF ve DOC için desteklenir.

 **Examples:** 

Metin yönünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
 // to the right so that all left-to-right text now goes top-to-bottom.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTextOrientation(TextOrientation.UPWARD);

 doc.save(getArtifactsDir() + "PageSetup.SetTextOrientation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [TextOrientation](../../com.aspose.words/textorientation/) sabitlerinden biri olmalıdır. |

### setTopMargin(double value) {#setTopMargin-double}
```
public void setTopMargin(double value)
```


Sayfanın üst kenarı ile gövde metninin üst sınırı arasındaki mesafeyi (nokta cinsinden) ayarlar.

 **Examples:** 

Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Sayfanın üst kenarı ile gövde metnin üst sınırı arasındaki mesafe (puan cinsinden). |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Bir belge veya bölümdeki her sayfadaki metnin dikey hizalamasını ayarlar.

 **Examples:** 

Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma işlemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bir belge veya bölümdeki her sayfadaki metnin dikey hizalaması. Değer, [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/) sabitlerinden biri olmalıdır. |

