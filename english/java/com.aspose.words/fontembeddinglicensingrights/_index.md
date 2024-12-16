---
title: FontEmbeddingLicensingRights
linktitle: FontEmbeddingLicensingRights
second_title: Aspose.Words for Java
description: Represents embedding licensing rights for the font in Java.
type: docs
weight: 314
url: /java/com.aspose.words/fontembeddinglicensingrights/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingLicensingRights
```

Represents embedding licensing rights for the font.

 **Remarks:** 

To learn more, visit the [ OpenType specification section ][OpenType specification section] on Microsoft Typography portal.


[OpenType specification section]: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype
## Methods

| Method | Description |
| --- | --- |
| [getBitmapEmbeddingOnly()](#getBitmapEmbeddingOnly) | Indicates the "Bitmap embedding only" restriction. |
| [getEmbeddingUsagePermissions()](#getEmbeddingUsagePermissions) | Usage permissions. |
| [getNoSubsetting()](#getNoSubsetting) | Indicates the "No subsetting" restriction. |
### getBitmapEmbeddingOnly() {#getBitmapEmbeddingOnly}
```
public boolean getBitmapEmbeddingOnly()
```


Indicates the "Bitmap embedding only" restriction.

 **Remarks:** 

When this bit is set, only bitmaps contained in the font may be embedded. No outline data may be embedded. If there are no bitmaps available in the font, then the font is considered unembeddable and the embedding services will fail. Other embedding restrictions also apply.

 **Examples:** 

Shows how to get license rights information for embedded fonts (FontInfo).

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
boolean - The corresponding  boolean  value.
### getEmbeddingUsagePermissions() {#getEmbeddingUsagePermissions}
```
public int getEmbeddingUsagePermissions()
```


Usage permissions.

 **Examples:** 

Shows how to get license rights information for embedded fonts (FontInfo).

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
int - The corresponding  int  value. The returned value is one of [FontEmbeddingUsagePermissions](../../com.aspose.words/fontembeddingusagepermissions/) constants.
### getNoSubsetting() {#getNoSubsetting}
```
public boolean getNoSubsetting()
```


Indicates the "No subsetting" restriction.

 **Remarks:** 

When this flag is set, the font must not be subsetted prior to embedding. Other embedding restrictions also apply.

 **Examples:** 

Shows how to get license rights information for embedded fonts (FontInfo).

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
boolean - The corresponding  boolean  value.
