---
title: "FontEmbeddingLicensingRights"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words para Java"
description: "Representa los derechos de licencia de incrustación para la fuente en Java."
type: docs
weight: 321
url: /es/java/com.aspose.words/fontembeddinglicensingrights/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingLicensingRights
```

Representa los derechos de licencia de incrustación para la fuente.

 **Remarks:** 

Para obtener más información, visite la [ OpenType specification section ][OpenType specification section] en el portal Microsoft Typography.

 **Examples:** 

Muestra cómo obtener información de derechos de licencia para fuentes incrustadas (FontInfo).

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getBitmapEmbeddingOnly()](#getBitmapEmbeddingOnly) | Indica la restricción \"Bitmap embedding only\". |
| [getEmbeddingUsagePermissions()](#getEmbeddingUsagePermissions) | Permisos de uso. |
| [getNoSubsetting()](#getNoSubsetting) | Indica la restricción \"No subsetting\". |
### getBitmapEmbeddingOnly() {#getBitmapEmbeddingOnly}
```
public boolean getBitmapEmbeddingOnly()
```


Indica la restricción \"Bitmap embedding only\".

 **Remarks:** 

Cuando este bit está activado, solo se pueden incrustar los mapas de bits contenidos en la fuente. No se pueden incrustar datos de contorno. Si no hay mapas de bits disponibles en la fuente, entonces la fuente se considera no incrustable y los servicios de incrustación fallarán. También se aplican otras restricciones de incrustación.

 **Examples:** 

Muestra cómo obtener información de derechos de licencia para fuentes incrustadas (FontInfo).

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
boolean - El valor  boolean  correspondiente.
### getEmbeddingUsagePermissions() {#getEmbeddingUsagePermissions}
```
public int getEmbeddingUsagePermissions()
```


Permisos de uso.

 **Examples:** 

Muestra cómo obtener información de derechos de licencia para fuentes incrustadas (FontInfo).

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
int - El valor int correspondiente. El valor devuelto es una de las constantes de [FontEmbeddingUsagePermissions](../../com.aspose.words/fontembeddingusagepermissions/).
### getNoSubsetting() {#getNoSubsetting}
```
public boolean getNoSubsetting()
```


Indica la restricción \"No subsetting\".

 **Remarks:** 

Cuando esta bandera está activada, la fuente no debe subestablecerse antes de incrustarla. También se aplican otras restricciones de incrustación.

 **Examples:** 

Muestra cómo obtener información de derechos de licencia para fuentes incrustadas (FontInfo).

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
boolean - El valor  boolean  correspondiente.
