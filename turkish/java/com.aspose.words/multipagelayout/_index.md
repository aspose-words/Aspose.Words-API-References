---
title: "MultiPageLayout"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words Java için"
description: "Java'da birden çok sayfayı tek bir çıktıya işlemek için bir yerleşim tanımlar."
type: docs
weight: 472
url: /tr/java/com.aspose.words/multipagelayout/
---

**Inheritance:**
java.lang.Object
```
public class MultiPageLayout
```

Birden çok sayfanın tek bir çıktıya işlenmesi için bir düzen tanımlar.

 **Remarks:** 

Bir yerleşim yapılandırması oluşturmak için statik fabrikasyon yöntemlerinden birini kullanın.

 **Examples:** 

Belgeyi çok sayfalı yerleşim ayarlarıyla JPG görüntüsü olarak kaydetmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set up a grid layout with:
 // - 3 columns per row.
 // - 10pts spacing between pages (horizontal and vertical).
 options.setPageLayout(MultiPageLayout.grid(3, 10f, 10f));

 // Alternative layouts:
 // options.PageLayout = MultiPageLayout.Horizontal(10);
 // options.PageLayout = MultiPageLayout.Vertical(10);

 // Customize the background and border.
 options.getPageLayout().setBackColor(Color.lightGray);
 options.getPageLayout().setBorderColor(Color.BLUE);
 options.getPageLayout().setBorderWidth(2f);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GridLayout.jpg", options);
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBackColor()](#getBackColor) | Çıktının arka plan rengini alır. |
| [getBorderColor()](#getBorderColor) | Sayfaların kenarlık rengini alır. |
| [getBorderWidth()](#getBorderWidth) | Sayfaların kenarlık genişliğini alır. |
| [grid(int columns, float horizontalGap, float verticalGap)](#grid-int-float-float) | Sayfaların soldan sağa, üstten alta, belirtilen sütun sayısıyla bir ızgara içinde işleneceği bir yerleşim oluşturur. |
| [horizontal(float horizontalGap)](#horizontal-float) | Belirtilen tüm sayfaların yan yana, soldan sağa tek bir çıktıda yatay olarak işleneceği bir yerleşim oluşturur. |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Çıktının arka plan rengini ayarlar. |
| [setBorderColor(Color value)](#setBorderColor-java.awt.Color) | Sayfaların kenarlık rengini ayarlar. |
| [setBorderWidth(float value)](#setBorderWidth-float) | Sayfaların kenarlık genişliğini ayarlar. |
| [singlePage()](#singlePage) | Belirtilen sayfalardan yalnızca ilkini işleyen bir yerleşim oluşturur. |
| [tiffFrames()](#tiffFrames) | Her sayfanın çok çerçeveli bir TIFF görüntüsünde ayrı bir çerçeve olarak işlendiği bir yerleşim oluşturur. |
| [vertical(float verticalGap)](#vertical-float) | Belirtilen tüm sayfaların tek bir çıktıda dikey olarak, biri diğerinin altında işleneceği bir yerleşim oluşturur. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Çıktının arka plan rengini alır. Varsayılan java.awt.Color\#EMPTY.EMPTY'dir.

**Returns:**
java.awt.Color - Çıktının arka plan rengi.
### getBorderColor() {#getBorderColor}
```
public Color getBorderColor()
```


Sayfaların kenarlık rengini alır. Varsayılan java.awt.Color\#EMPTY.EMPTY'dir.

**Returns:**
java.awt.Color - Sayfaların kenarlık rengi.
### getBorderWidth() {#getBorderWidth}
```
public float getBorderWidth()
```


Sayfa kenarlığının genişliğini alır. Varsayılan değer 0'dır.

**Returns:**
float - Sayfa kenarlığının genişliği.
### grid(int columns, float horizontalGap, float verticalGap) {#grid-int-float-float}
```
public static MultiPageLayout grid(int columns, float horizontalGap, float verticalGap)
```


Sayfaların soldan sağa, üstten alta, belirtilen sütun sayısıyla bir ızgara içinde işleneceği bir yerleşim oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sütunlar | int | Yerleşimdeki sütun sayısı. Sıfırdan büyük olmalıdır. |
| horizontalGap | float | Sütunlar arasındaki yatay boşluk (nokta cinsinden). |
| verticalGap | float | Satırlar arasındaki dikey boşluk (nokta cinsinden). |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### horizontal(float horizontalGap) {#horizontal-float}
```
public static MultiPageLayout horizontal(float horizontalGap)
```


Belirtilen tüm sayfaların yan yana, soldan sağa tek bir çıktıda yatay olarak işleneceği bir yerleşim oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| horizontalGap | float | Sayfalar arasındaki yatay boşluk (nokta cinsinden). |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Çıktının arka plan rengini ayarlar. Varsayılan değer java.awt.Color\\#EMPTY.EMPTY.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Çıktının arka plan rengi. |

### setBorderColor(Color value) {#setBorderColor-java.awt.Color}
```
public void setBorderColor(Color value)
```


Sayfa kenarlığının rengini ayarlar. Varsayılan değer java.awt.Color\\#EMPTY.EMPTY.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Sayfa kenarlığının rengi. |

### setBorderWidth(float value) {#setBorderWidth-float}
```
public void setBorderWidth(float value)
```


Sayfa kenarlığının genişliğini ayarlar. Varsayılan değer 0.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | float | Sayfa kenarlığının genişliği. |

### singlePage() {#singlePage}
```
public static MultiPageLayout singlePage()
```


Belirtilen sayfalardan yalnızca ilkini işleyen bir yerleşim oluşturur.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### tiffFrames() {#tiffFrames}
```
public static MultiPageLayout tiffFrames()
```


Her sayfanın çok çerçeveli bir TIFF görüntüsünde ayrı bir çerçeve olarak işlendiği bir yerleşim oluşturur. Yalnızca TIFF görüntü formatları için geçerlidir.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### vertical(float verticalGap) {#vertical-float}
```
public static MultiPageLayout vertical(float verticalGap)
```


Belirtilen tüm sayfaların tek bir çıktıda dikey olarak, biri diğerinin altında işleneceği bir yerleşim oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| verticalGap | float | Sayfalar arasındaki dikey boşluk (nokta cinsinden). |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
