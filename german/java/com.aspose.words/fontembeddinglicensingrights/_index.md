---
title: "FontEmbeddingLicensingRights"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words für Java"
description: "Stellt die Einbettungs-Lizenzrechte für die Schriftart in Java dar."
type: docs
weight: 321
url: /de/java/com.aspose.words/fontembeddinglicensingrights/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingLicensingRights
```

Stellt die Einbettungs‑Lizenzrechte für die Schrift dar.

 **Remarks:** 

Um mehr zu erfahren, besuchen Sie den [ OpenType specification section ][OpenType specification section] auf dem Microsoft Typography-Portal.

 **Examples:** 

Zeigt, wie man Lizenzrechtsinformationen für eingebettete Schriftarten (FontInfo) abruft.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBitmapEmbeddingOnly()](#getBitmapEmbeddingOnly) | Gibt die Einschränkung "Bitmap-Einbettung nur" an. |
| [getEmbeddingUsagePermissions()](#getEmbeddingUsagePermissions) | Nutzungsberechtigungen. |
| [getNoSubsetting()](#getNoSubsetting) | Gibt die Einschränkung "Kein Subsetting" an. |
### getBitmapEmbeddingOnly() {#getBitmapEmbeddingOnly}
```
public boolean getBitmapEmbeddingOnly()
```


Gibt die Einschränkung "Bitmap-Einbettung nur" an.

 **Remarks:** 

Wenn dieses Bit gesetzt ist, dürfen nur Bitmaps, die in der Schriftart enthalten sind, eingebettet werden. Es dürfen keine Konturdaten eingebettet werden. Wenn keine Bitmaps in der Schriftart verfügbar sind, wird die Schriftart als nicht einbettbar betrachtet und die Einbettungsdienste werden fehlschlagen. Weitere Einbettungsbeschränkungen gelten ebenfalls.

 **Examples:** 

Zeigt, wie man Lizenzrechtsinformationen für eingebettete Schriftarten (FontInfo) abruft.

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
boolean - Der entsprechende  boolean  Wert.
### getEmbeddingUsagePermissions() {#getEmbeddingUsagePermissions}
```
public int getEmbeddingUsagePermissions()
```


Nutzungsberechtigungen.

 **Examples:** 

Zeigt, wie man Lizenzrechtsinformationen für eingebettete Schriftarten (FontInfo) abruft.

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
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [FontEmbeddingUsagePermissions](../../com.aspose.words/fontembeddingusagepermissions/).
### getNoSubsetting() {#getNoSubsetting}
```
public boolean getNoSubsetting()
```


Gibt die Einschränkung "Kein Subsetting" an.

 **Remarks:** 

Wenn dieses Flag gesetzt ist, darf die Schriftart vor dem Einbetten nicht unterteilt werden. Weitere Einbettungsbeschränkungen gelten ebenfalls.

 **Examples:** 

Zeigt, wie man Lizenzrechtsinformationen für eingebettete Schriftarten (FontInfo) abruft.

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
boolean - Der entsprechende  boolean  Wert.
