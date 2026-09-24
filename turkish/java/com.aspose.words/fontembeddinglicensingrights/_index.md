---
title: "FontEmbeddingLicensingRights"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words Java için"
description: "Java'da font için gömme lisans haklarını temsil eder."
type: docs
weight: 321
url: /tr/java/com.aspose.words/fontembeddinglicensingrights/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingLicensingRights
```

Yazı tipi için gömme lisans haklarını temsil eder.

 **Remarks:** 

Daha fazla bilgi edinmek için Microsoft Typography portalındaki [ OpenType specification section ][OpenType specification section] sayfasını ziyaret edin.

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


[OpenType specification section]: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBitmapEmbeddingOnly()](#getBitmapEmbeddingOnly) | "Bitmap embedding only" kısıtlamasını gösterir. |
| [getEmbeddingUsagePermissions()](#getEmbeddingUsagePermissions) | Kullanım izinleri. |
| [getNoSubsetting()](#getNoSubsetting) | "No subsetting" kısıtlamasını gösterir. |
### getBitmapEmbeddingOnly() {#getBitmapEmbeddingOnly}
```
public boolean getBitmapEmbeddingOnly()
```


"Bitmap embedding only" kısıtlamasını gösterir.

 **Remarks:** 

Bu bit ayarlandığında, yalnızca fontta bulunan bitmapler gömülebilir. Kontur verileri gömülemez. Fontta bitmap bulunmuyorsa, font gömülemez kabul edilir ve gömme hizmetleri başarısız olur. Diğer gömme kısıtlamaları da geçerlidir.

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
boolean - İlgili  boolean  değeri.
### getEmbeddingUsagePermissions() {#getEmbeddingUsagePermissions}
```
public int getEmbeddingUsagePermissions()
```


Kullanım izinleri.

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
int - İlgili int değeri. Döndürülen değer, [FontEmbeddingUsagePermissions](../../com.aspose.words/fontembeddingusagepermissions/) sabitlerinden biridir.
### getNoSubsetting() {#getNoSubsetting}
```
public boolean getNoSubsetting()
```


"No subsetting" kısıtlamasını gösterir.

 **Remarks:** 

Bu bayrak ayarlandığında, font gömülmeden önce alt kümeleme yapılmamalıdır. Diğer gömme kısıtlamaları da geçerlidir.

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
boolean - İlgili  boolean  değeri.
