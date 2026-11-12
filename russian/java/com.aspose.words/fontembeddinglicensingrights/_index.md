---
title: "FontEmbeddingLicensingRights"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words для Java"
description: "Представляет права лицензирования встраивания шрифта в Java."
type: docs
weight: 321
url: /ru/java/com.aspose.words/fontembeddinglicensingrights/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingLicensingRights
```

Представляет права лицензии на встраивание шрифта.

 **Remarks:** 

Чтобы узнать больше, посетите [ OpenType specification section ][OpenType specification section] на портале Microsoft Typography.

 **Examples:** 

Показывает, как получить информацию о правах лицензии для внедрённых шрифтов (FontInfo).

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
## Методы

| Метод | Описание |
| --- | --- |
| [getBitmapEmbeddingOnly()](#getBitmapEmbeddingOnly) | Указывает ограничение «Только встраивание растровых изображений». |
| [getEmbeddingUsagePermissions()](#getEmbeddingUsagePermissions) | Разрешения на использование. |
| [getNoSubsetting()](#getNoSubsetting) | Указывает ограничение «Без подмножества». |
### getBitmapEmbeddingOnly() {#getBitmapEmbeddingOnly}
```
public boolean getBitmapEmbeddingOnly()
```


Указывает ограничение «Только встраивание растровых изображений».

 **Remarks:** 

Когда этот бит установлен, могут быть встроены только растровые изображения, содержащиеся в шрифте. Контурные данные встраиваться не могут. Если в шрифте нет доступных растровых изображений, шрифт считается не встраиваемым, и службы встраивания завершатся с ошибкой. Также применяются другие ограничения на встраивание.

 **Examples:** 

Показывает, как получить информацию о правах лицензии для внедрённых шрифтов (FontInfo).

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
boolean - Соответствующее  boolean  значение.
### getEmbeddingUsagePermissions() {#getEmbeddingUsagePermissions}
```
public int getEmbeddingUsagePermissions()
```


Разрешения на использование.

 **Examples:** 

Показывает, как получить информацию о правах лицензии для внедрённых шрифтов (FontInfo).

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
int — соответствующее значение типа int. Возвращаемое значение является одной из констант [FontEmbeddingUsagePermissions](../../com.aspose.words/fontembeddingusagepermissions/).
### getNoSubsetting() {#getNoSubsetting}
```
public boolean getNoSubsetting()
```


Указывает ограничение «Без подмножества».

 **Remarks:** 

Когда этот флаг установлен, шрифт не должен быть подмножен перед встраиванием. Также применяются другие ограничения на встраивание.

 **Examples:** 

Показывает, как получить информацию о правах лицензии для внедрённых шрифтов (FontInfo).

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
boolean - Соответствующее  boolean  значение.
