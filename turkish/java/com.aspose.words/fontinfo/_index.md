---
title: "FontInfo"
linktitle: "FontInfo"
second_title: "Aspose.Words Java için"
description: "Java'da belgede kullanılan bir yazı tipi hakkında bilgi belirtir."
type: docs
weight: 326
url: /tr/java/com.aspose.words/fontinfo/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class FontInfo implements Cloneable
```

Belgede kullanılan bir yazı tipi hakkında bilgi belirtir.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu sınıfın örneklerini doğrudan oluşturamazsınız. Bir belgede tanımlı yazı tipleri koleksiyonuna erişmek için [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) özelliğini kullanın.

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


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAltName()](#getAltName) | Yazı tipinin alternatif adını alır. |
| [getCharset()](#getCharset) | Yazı tipinin karakter kümesini alır. |
| [getEmbeddedFont(int format, int style)](#getEmbeddedFont-int-int) |  |
| [getEmbeddedFontAsOpenType(int style)](#getEmbeddedFontAsOpenType-int) |  |
| [getEmbeddingLicensingRights()](#getEmbeddingLicensingRights) | Gömülü yazı tipi lisans haklarını alır. |
| [getFamily()](#getFamily) | Bu yazı tipinin ait olduğu yazı tipi ailesini alır. |
| [getName()](#getName) | Yazı tipinin adını alır. |
| [getPanose()](#getPanose) | PANOSE yazı tipi sınıflandırma numarasını alır. |
| [getPitch()](#getPitch) | Aralık, yazı tipinin sabit aralıklı, orantılı aralıklı olup olmadığını veya varsayılan ayara dayanıp dayanmadığını gösterir. |
| [isTrueType()](#isTrueType) | Bu yazı tipinin raster veya vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu gösterir. |
| [isTrueType(boolean value)](#isTrueType-boolean) | Bu yazı tipinin raster veya vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu gösterir. |
| [setAltName(String value)](#setAltName-java.lang.String) | Yazı tipinin alternatif adını ayarlar. |
| [setCharset(int value)](#setCharset-int) | Yazı tipinin karakter kümesini ayarlar. |
| [setFamily(int value)](#setFamily-int) | Bu yazı tipinin ait olduğu yazı tipi ailesini ayarlar. |
| [setPanose(byte[] value)](#setPanose-byte) | PANOSE yazı tipi sınıflandırma numarasını ayarlar. |
| [setPitch(int value)](#setPitch-int) | Aralık, yazı tipinin sabit aralıklı, orantılı aralıklı olup olmadığını veya varsayılan ayara dayanıp dayanmadığını gösterir. |
### getAltName() {#getAltName}
```
public String getAltName()
```


Yazı tipinin alternatif adını alır.

 **Remarks:** 

null olamaz. Boş bir dize olabilir.

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
java.lang.String - Yazı tipinin alternatif adı.
### getCharset() {#getCharset}
```
public int getCharset()
```


Yazı tipinin karakter kümesini alır.

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
int - Yazı tipinin karakter kümesi.
### getEmbeddedFont(int format, int style) {#getEmbeddedFont-int-int}
```
public byte[] getEmbeddedFont(int format, int style)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| biçim | int |  |
| stil | int |  |

**Returns:**
byte[]
### getEmbeddedFontAsOpenType(int style) {#getEmbeddedFontAsOpenType-int}
```
public byte[] getEmbeddedFontAsOpenType(int style)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stil | int |  |

**Returns:**
byte[]
### getEmbeddingLicensingRights() {#getEmbeddingLicensingRights}
```
public FontEmbeddingLicensingRights getEmbeddingLicensingRights()
```


Gömülü yazı tipi lisans haklarını alır.

 **Remarks:** 

Yazı tipi gömülü değilse değer null olabilir.

 **Examples:** 

Gömülü yazı tipleri için lisans hakları bilgilerini (FontInfo) nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Embedded font rights.docx");

 // Get the list of document fonts.
 FontInfoCollection fontInfos = doc.getFontInfos();
 for (FontInfo fontInfo : fontInfos)
 {
     if (fontInfo.getEmbeddingLicensingRights() != null)
     {
         System.out.println(fontInfo.getEmbeddingLicensingRights().getEmbeddingUsagePermissions());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getBitmapEmbeddingOnly());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getNoSubsetting());
     }
 }
 
```

**Returns:**
[FontEmbeddingLicensingRights](../../com.aspose.words/fontembeddinglicensingrights/) - The embedded font licensing rights.
### getFamily() {#getFamily}
```
public int getFamily()
```


Bu yazı tipinin ait olduğu yazı tipi ailesini alır.

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
int - Bu yazı tipinin ait olduğu yazı tipi ailesi. Döndürülen değer [FontFamily](../../com.aspose.words/fontfamily/) sabitlerinden biridir.
### getName() {#getName}
```
public String getName()
```


Yazı tipinin adını alır.

 **Remarks:** 

null olamaz. Boş bir dize olabilir.

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

**Returns:**
java.lang.String - Yazı tipinin adı.
### getPanose() {#getPanose}
```
public byte[] getPanose()
```


PANOSE yazı tipi sınıflandırma numarasını alır.

 **Remarks:** 

PANOSE, bir yazı tipinin kontrast, ağırlık ve serif stili gibi kritik görsel özelliklerini tanımlayan kompakt 10-bytelık bir açıklamadır. Rakamlar Aile Türü, Serif Stili, Ağırlık, Oran, Kontrast, Çizgi Varyasyonu, Kol Stili, Harf Formu, Orta Çizgi ve X-Yüksekliğini temsil eder.

null olabilir.

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
byte[] - PANOSE yazı tipi sınıflandırma numarası.
### getPitch() {#getPitch}
```
public int getPitch()
```


Aralık, yazı tipinin sabit aralıklı, orantılı aralıklı olup olmadığını veya varsayılan ayara dayanıp dayanmadığını gösterir.

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
int - İlgili int değeri. Döndürülen değer [FontPitch](../../com.aspose.words/fontpitch/) sabitlerinden biridir.
### isTrueType() {#isTrueType}
```
public boolean isTrueType()
```


Bu yazı tipinin raster veya vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu gösterir. Varsayılan değer true'dur.

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

**Returns:**
boolean - İlgili  boolean  değeri.
### isTrueType(boolean value) {#isTrueType-boolean}
```
public void isTrueType(boolean value)
```


Bu yazı tipinin raster veya vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu gösterir. Varsayılan değer true'dur.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setAltName(String value) {#setAltName-java.lang.String}
```
public void setAltName(String value)
```


Yazı tipinin alternatif adını ayarlar.

 **Remarks:** 

null olamaz. Boş bir dize olabilir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Yazı tipinin alternatif adı. |

### setCharset(int value) {#setCharset-int}
```
public void setCharset(int value)
```


Yazı tipinin karakter kümesini ayarlar.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Yazı tipinin karakter kümesi. |

### setFamily(int value) {#setFamily-int}
```
public void setFamily(int value)
```


Bu yazı tipinin ait olduğu yazı tipi ailesini ayarlar.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu yazı tipinin ait olduğu yazı tipi ailesi. Değer [FontFamily](../../com.aspose.words/fontfamily/) sabitlerinden biri olmalıdır. |

### setPanose(byte[] value) {#setPanose-byte}
```
public void setPanose(byte[] value)
```


PANOSE yazı tipi sınıflandırma numarasını ayarlar.

 **Remarks:** 

PANOSE, bir yazı tipinin kontrast, ağırlık ve serif stili gibi kritik görsel özelliklerini tanımlayan kompakt 10-bytelık bir açıklamadır. Rakamlar Aile Türü, Serif Stili, Ağırlık, Oran, Kontrast, Çizgi Varyasyonu, Kol Stili, Harf Formu, Orta Çizgi ve X-Yüksekliğini temsil eder.

null olabilir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | byte[] | PANOSE yazı tipi sınıflandırma numarası. |

### setPitch(int value) {#setPitch-int}
```
public void setPitch(int value)
```


Aralık, yazı tipinin sabit aralıklı, orantılı aralıklı olup olmadığını veya varsayılan ayara dayanıp dayanmadığını gösterir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [FontPitch](../../com.aspose.words/fontpitch/) sabitlerinden biri olmalıdır. |

