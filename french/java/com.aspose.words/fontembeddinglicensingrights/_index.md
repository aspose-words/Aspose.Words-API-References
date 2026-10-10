---
title: "FontEmbeddingLicensingRights"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words pour Java"
description: "Représente les droits de licence d'intégration pour la police en Java."
type: docs
weight: 321
url: /fr/java/com.aspose.words/fontembeddinglicensingrights/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingLicensingRights
```

Représente les droits de licence d'intégration pour la police.

 **Remarks:** 

Pour en savoir plus, consultez la [ OpenType specification section ][OpenType specification section] sur le portail Microsoft Typography.

 **Examples:** 

Montre comment obtenir les informations de droits de licence pour les polices incorporées (FontInfo).

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getBitmapEmbeddingOnly()](#getBitmapEmbeddingOnly) | Indique la restriction "Bitmap embedding only". |
| [getEmbeddingUsagePermissions()](#getEmbeddingUsagePermissions) | Autorisations d'utilisation. |
| [getNoSubsetting()](#getNoSubsetting) | Indique la restriction "No subsetting". |
### getBitmapEmbeddingOnly() {#getBitmapEmbeddingOnly}
```
public boolean getBitmapEmbeddingOnly()
```


Indique la restriction "Bitmap embedding only".

 **Remarks:** 

Lorsque ce bit est activé, seuls les bitmaps contenus dans la police peuvent être intégrés. Aucune donnée de contour ne peut être intégrée. S'il n'y a aucun bitmap disponible dans la police, celle-ci est considérée comme non intégrable et les services d'intégration échoueront. D'autres restrictions d'intégration s'appliquent également.

 **Examples:** 

Montre comment obtenir les informations de droits de licence pour les polices incorporées (FontInfo).

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
boolean - La valeur  boolean  correspondante.
### getEmbeddingUsagePermissions() {#getEmbeddingUsagePermissions}
```
public int getEmbeddingUsagePermissions()
```


Autorisations d'utilisation.

 **Examples:** 

Montre comment obtenir les informations de droits de licence pour les polices incorporées (FontInfo).

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
int - La valeur int correspondante. La valeur retournée est l'une des constantes [FontEmbeddingUsagePermissions](../../com.aspose.words/fontembeddingusagepermissions/).
### getNoSubsetting() {#getNoSubsetting}
```
public boolean getNoSubsetting()
```


Indique la restriction "No subsetting".

 **Remarks:** 

Lorsque ce drapeau est activé, la police ne doit pas être sous‑ensemble avant l'intégration. D'autres restrictions d'intégration s'appliquent également.

 **Examples:** 

Montre comment obtenir les informations de droits de licence pour les polices incorporées (FontInfo).

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
boolean - La valeur  boolean  correspondante.
