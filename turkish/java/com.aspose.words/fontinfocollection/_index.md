---
title: "FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgede kullanılan yazı tiplerinin bir koleksiyonunu temsil eder."
type: docs
weight: 327
url: /tr/java/com.aspose.words/fontinfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

Belgede kullanılan yazı tiplerinin bir koleksiyonunu temsil eder.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Ögeler [FontInfo](../../com.aspose.words/fontinfo/) nesneleridir.

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Belgede tanımlı yazı tipleri koleksiyonuna erişmek için [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) özelliğini kullanın.

 **Examples:** 

Bir belgede bulunan yazı tiplerinin ayrıntılarını nasıl yazdıracağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

Gömülü TrueType yazı tipleriyle bir belgenin nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [contains(String name)](#contains-java.lang.String) | Koleksiyonun verilen ada sahip bir yazı tipi içerip içermediğini belirler. |
| [get(int index)](#get-int) | Belirtilen indeksteki bir yazı tipini alır. |
| [get(String name)](#get-java.lang.String) | Koleksiyon öğelerine erişim sağlar. |
| [getCount()](#getCount) | Koleksiyonda bulunan öğe sayısını alır. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts) | Sistem yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts) | Belge kaydedildiğinde TrueType yazı tiplerinin gömülüp gömülmeyeceğini belirtir. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts) | Gömülü TrueType yazı tiplerinin bir alt kümesinin belgeyle birlikte kaydedilip kaydedilmeyeceğini belirtir. |
| [iterator()](#iterator) | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür. |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean) | Sistem yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean) | Belge kaydedildiğinde TrueType yazı tiplerinin gömülüp gömülmeyeceğini belirtir. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean) | Gömülü TrueType yazı tiplerinin bir alt kümesinin belgeyle birlikte kaydedilip kaydedilmeyeceğini belirtir. |
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Koleksiyonun verilen ada sahip bir yazı tipi içerip içermediğini belirler.

 **Examples:** 

Boş belgede bulunan yazı tipleri hakkında bilgi gösterir.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Bulunacak yazı tipinin büyük/küçük harfe duyarsız adı. |

**Returns:**
boolean -  true  eğer öğe koleksiyonda bulunursa; aksi takdirde,  false .
### get(int index) {#get-int}
```
public FontInfo get(int index)
```


Belirtilen indeksteki bir yazı tipini alır.

 **Examples:** 

Gömülü bir yazı tipinin bir belgeden nasıl çıkarılacağını ve yerel dosya sistemine nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Yazı tipinin sıfır tabanlı indeksi. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - A font at the specified index.
### get(String name) {#get-java.lang.String}
```
public FontInfo get(String name)
```


Koleksiyon öğelerine erişim sağlar.  Belirtilen ada sahip bir yazı tipini alır.

 **Examples:** 

Gömülü bir yazı tipinin bir belgeden nasıl çıkarılacağını ve yerel dosya sistemine nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Bulunacak yazı tipinin büyük/küçük harfe duyarsız adı. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - The corresponding [FontInfo](../../com.aspose.words/fontinfo/) value.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyonda bulunan öğe sayısını alır.

 **Examples:** 

Boş belgede bulunan yazı tipleri hakkında bilgi gösterir.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Returns:**
int - Koleksiyonda bulunan öğe sayısı.
### getEmbedSystemFonts() {#getEmbedSystemFonts}
```
public boolean getEmbedSystemFonts()
```


Sistem yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri  false  dır.

Bu seçenek yalnızca [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) seçeneği  true  olarak ayarlandığında çalışır.

 **Remarks:** 

Bu özelliği  true  olarak ayarlamak, kullanıcının Doğu Asya sisteminde olması ve sisteminde o dil için yazı tipleri olmayan diğer kişiler tarafından okunabilir bir belge oluşturmak istemesi durumunda faydalıdır. Örneğin, Japonya sisteminde bir kullanıcı, Japonca belgenin tüm sistemlerde okunabilir olmasını sağlamak için yazı tiplerini belgeye gömmeyi seçebilir.

Bu seçenek yalnızca DOC, DOCX ve RTF formatları için çalışır.

 **Examples:** 

Gömülü TrueType yazı tipleriyle bir belgenin nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts}
```
public boolean getEmbedTrueTypeFonts()
```


Belge kaydedildiğinde TrueType yazı tiplerinin gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri  false  dır.

 **Remarks:** 

TrueType yazı tiplerini gömmek, başkalarının belgeyi oluşturulurken kullanılan aynı yazı tipleriyle görüntülemesini sağlar, ancak belge boyutunu önemli ölçüde artırabilir.

Bu seçenek yalnızca DOC, DOCX ve RTF formatları için çalışır.

 **Examples:** 

Gömülü TrueType yazı tipleriyle bir belgenin nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getSaveSubsetFonts() {#getSaveSubsetFonts}
```
public boolean getSaveSubsetFonts()
```


Gömülü TrueType yazı tiplerinin bir alt kümesinin belgeyle birlikte kaydedilip kaydedilmeyeceğini belirtir. Bu özelliğin varsayılan değeri  false  dır.

Bu seçenek yalnızca [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) özelliği  true  olarak ayarlandığında çalışır.

 **Remarks:** 

Bu seçenek yalnızca DOC, DOCX ve RTF formatları için çalışır.

 **Examples:** 

Gömülü TrueType yazı tipleriyle bir belgenin nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### iterator() {#iterator}
```
public Iterator iterator()
```


Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür.

 **Examples:** 

Bir belgede her yazı tipine nasıl erişileceğini ve ayrıntıların nasıl yazdırılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Iterator fontCollectionEnumerator = doc.getFontInfos().iterator();
 while (fontCollectionEnumerator.hasNext()) {
     FontInfo fontInfo = fontCollectionEnumerator.next();
     if (fontInfo != null) {
         System.out.println("Font name: " + fontInfo.getName());

         // Alt names are usually blank.
         System.out.println("Alt name: " + fontInfo.getAltName());
         System.out.println("\t- Family: " + fontInfo.getFamily());
         System.out.println("\t- " + (fontInfo.isTrueType() ? "Is TrueType" : "Is not TrueType"));
         System.out.println("\t- Pitch: " + fontInfo.getPitch());
         System.out.println("\t- Charset: " + fontInfo.getCharset());
         System.out.println("\t- Panose:");
         System.out.println("\t\tFamily Kind: " + (fontInfo.getPanose()[0] & 0xFF));
         System.out.println("\t\tSerif Style: " + (fontInfo.getPanose()[1] & 0xFF));
         System.out.println("\t\tWeight: " + (fontInfo.getPanose()[2] & 0xFF));
         System.out.println("\t\tProportion: " + (fontInfo.getPanose()[3] & 0xFF));
         System.out.println("\t\tContrast: " + (fontInfo.getPanose()[4] & 0xFF));
         System.out.println("\t\tStroke Variation: " + (fontInfo.getPanose()[5] & 0xFF));
         System.out.println("\t\tArm Style: " + (fontInfo.getPanose()[6] & 0xFF));
         System.out.println("\t\tLetterform: " + (fontInfo.getPanose()[7] & 0xFF));
         System.out.println("\t\tMidline: " + (fontInfo.getPanose()[8] & 0xFF));
         System.out.println("\t\tX-Height: " + (fontInfo.getPanose()[9] & 0xFF));
     }
 }
 
```

**Returns:**
java.util.Iterator
### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean}
```
public void setEmbedSystemFonts(boolean value)
```


Sistem yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri  false  dır.

Bu seçenek yalnızca [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) seçeneği  true  olarak ayarlandığında çalışır.

 **Remarks:** 

Bu özelliği  true  olarak ayarlamak, kullanıcının Doğu Asya sisteminde olması ve sisteminde o dil için yazı tipleri olmayan diğer kişiler tarafından okunabilir bir belge oluşturmak istemesi durumunda faydalıdır. Örneğin, Japonya sisteminde bir kullanıcı, Japonca belgenin tüm sistemlerde okunabilir olmasını sağlamak için yazı tiplerini belgeye gömmeyi seçebilir.

Bu seçenek yalnızca DOC, DOCX ve RTF formatları için çalışır.

 **Examples:** 

Gömülü TrueType yazı tipleriyle bir belgenin nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean}
```
public void setEmbedTrueTypeFonts(boolean value)
```


Belge kaydedildiğinde TrueType yazı tiplerinin gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri  false  dır.

 **Remarks:** 

TrueType yazı tiplerini gömmek, başkalarının belgeyi oluşturulurken kullanılan aynı yazı tipleriyle görüntülemesini sağlar, ancak belge boyutunu önemli ölçüde artırabilir.

Bu seçenek yalnızca DOC, DOCX ve RTF formatları için çalışır.

 **Examples:** 

Gömülü TrueType yazı tipleriyle bir belgenin nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean}
```
public void setSaveSubsetFonts(boolean value)
```


Gömülü TrueType yazı tiplerinin bir alt kümesinin belgeyle birlikte kaydedilip kaydedilmeyeceğini belirtir. Bu özelliğin varsayılan değeri  false  dır.

Bu seçenek yalnızca [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) özelliği  true  olarak ayarlandığında çalışır.

 **Remarks:** 

Bu seçenek yalnızca DOC, DOCX ve RTF formatları için çalışır.

 **Examples:** 

Gömülü TrueType yazı tipleriyle bir belgenin nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

