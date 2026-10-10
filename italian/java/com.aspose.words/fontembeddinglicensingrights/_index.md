---
title: "FontEmbeddingLicensingRights"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words per Java"
description: "Rappresenta i diritti di licenza di incorporamento per il font in Java."
type: docs
weight: 321
url: /it/java/com.aspose.words/fontembeddinglicensingrights/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingLicensingRights
```

Rappresenta i diritti di licenza di incorporamento per il font.

 **Remarks:** 

Per saperne di più, visita la [ OpenType specification section ][OpenType specification section] sul portale Microsoft Typography.

 **Examples:** 

Mostra come ottenere le informazioni sui diritti di licenza per i caratteri incorporati (FontInfo).

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getBitmapEmbeddingOnly()](#getBitmapEmbeddingOnly) | Indica la restrizione "Bitmap embedding only". |
| [getEmbeddingUsagePermissions()](#getEmbeddingUsagePermissions) | Permessi di utilizzo. |
| [getNoSubsetting()](#getNoSubsetting) | Indica la restrizione "No subsetting". |
### getBitmapEmbeddingOnly() {#getBitmapEmbeddingOnly}
```
public boolean getBitmapEmbeddingOnly()
```


Indica la restrizione "Bitmap embedding only".

 **Remarks:** 

Quando questo bit è impostato, solo i bitmap contenuti nel font possono essere incorporati. Nessun dato di contorno può essere incorporato. Se non sono disponibili bitmap nel font, il font è considerato non incorporabile e i servizi di incorporamento falliranno. Si applicano anche altre restrizioni di incorporamento.

 **Examples:** 

Mostra come ottenere le informazioni sui diritti di licenza per i caratteri incorporati (FontInfo).

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
boolean - Il valore booleano corrispondente.
### getEmbeddingUsagePermissions() {#getEmbeddingUsagePermissions}
```
public int getEmbeddingUsagePermissions()
```


Permessi di utilizzo.

 **Examples:** 

Mostra come ottenere le informazioni sui diritti di licenza per i caratteri incorporati (FontInfo).

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
int - Il valore int corrispondente. Il valore restituito è una delle costanti [FontEmbeddingUsagePermissions](../../com.aspose.words/fontembeddingusagepermissions/).
### getNoSubsetting() {#getNoSubsetting}
```
public boolean getNoSubsetting()
```


Indica la restrizione "No subsetting".

 **Remarks:** 

Quando questo flag è impostato, il font non deve essere sottoposto a subset prima dell'incorporamento. Si applicano anche altre restrizioni di incorporamento.

 **Examples:** 

Mostra come ottenere le informazioni sui diritti di licenza per i caratteri incorporati (FontInfo).

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
boolean - Il valore booleano corrispondente.
