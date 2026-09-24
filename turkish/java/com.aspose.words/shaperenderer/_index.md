---
title: "ShapeRenderer"
linktitle: "ShapeRenderer"
second_title: "Aspose.Words Java için"
description: "Java'da bireysel bir Shape veya GroupShape'i raster veya vektör görüntüye veya bir Graphics nesnesine render etmek için yöntemler sağlar."
type: docs
weight: 616
url: /tr/java/com.aspose.words/shaperenderer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeRendererBase](../../com.aspose.words/noderendererbase/)
```
public class ShapeRenderer extends NodeRendererBase
```

Bireysel bir [Shape](../../com.aspose.words/shape/) veya [GroupShape](../../com.aspose.words/groupshape/) nesnesini raster veya vektör görüntüye veya bir Graphics nesnesine render etmek için yöntemler sağlar.

Daha fazla bilgi edinmek için [ Working with Shapes ][Working with Shapes] dokümantasyon makalesini ziyaret edin.


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [ShapeRenderer(ShapeBase shape)](#ShapeRenderer-com.aspose.words.ShapeBase) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBoundsInPixels(float scale, float dpi)](#getBoundsInPixels-float-float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını piksel cinsinden hesaplar. |
| [getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getBoundsInPixels-float-float-float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını piksel cinsinden hesaplar. |
| [getBoundsInPoints()](#getBoundsInPoints) | Şeklin gerçek sınırlarını nokta cinsinden alır. |
| [getOpaqueBoundsInPixels(float scale, float dpi)](#getOpaqueBoundsInPixels-float-float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını piksel cinsinden hesaplar. |
| [getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getOpaqueBoundsInPixels-float-float-float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını piksel cinsinden hesaplar. |
| [getOpaqueBoundsInPoints()](#getOpaqueBoundsInPoints) | Şeklin opak sınırlarını nokta cinsinden alır. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu piksel cinsinden hesaplar. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu piksel cinsinden hesaplar. |
| [getSizeInPoints()](#getSizeInPoints) | Şeklin gerçek boyutunu nokta cinsinden alır. |
| [renderToScale(Graphics2D graphics, float x, float y, float scale)](#renderToScale-java.awt.Graphics2D-float-float-float) | Şekli belirtilen ölçeğe göre bir java.awt.Graphics2D nesnesine render eder. |
| [renderToSize(Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-java.awt.Graphics2D-float-float-float-float) | Şekli belirtilen boyuta göre bir java.awt.Graphics2D nesnesine render eder. |
| [save(OutputStream stream, ImageSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions) |  |
| [save(OutputStream stream, SvgSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions) |  |
| [save(String fileName, ImageSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.ImageSaveOptions) | Şekli render eder ve bir görüntüye kaydeder. |
| [save(String fileName, SvgSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SvgSaveOptions) | Şekli render eder ve bir SVG görüntüsüne kaydeder. |
### ShapeRenderer(ShapeBase shape) {#ShapeRenderer-com.aspose.words.ShapeBase}
```
public ShapeRenderer(ShapeBase shape)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shape | [ShapeBase](../../com.aspose.words/shapebase/) | Render etmek istediğiniz DrawinML şekil nesnesi. |

### getBoundsInPixels(float scale, float dpi) {#getBoundsInPixels-float-float}
```
public Rectangle getBoundsInPixels(float scale, float dpi)
```


Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını piksel cinsinden hesaplar.

 **Remarks:** 

Bu yöntem [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) metodunu piksel cinsinden bir dikdörtgene dönüştürür.

 **Examples:** 

Şekilleri ölçme ve ölçeklendirme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ölçek | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| dpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için çözünürlük (yatay ve dikey). |

**Returns:**
java.awt.Rectangle - Şeklin piksel cinsinden gerçek (sayfada render edildiği gibi) sınırlama kutusu.
### getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getBoundsInPixels-float-float-float}
```
public Rectangle getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını piksel cinsinden hesaplar.

 **Remarks:** 

Bu yöntem [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) metodunu piksel cinsinden bir dikdörtgene dönüştürür.

 **Examples:** 

Şekilleri ölçme ve ölçeklendirme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ölçek | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| horizontalDpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için yatay çözünürlük. |
| verticalDpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için dikey çözünürlük. |

**Returns:**
java.awt.Rectangle - Şeklin piksel cinsinden gerçek (sayfada render edildiği gibi) sınırlama kutusu.
### getBoundsInPoints() {#getBoundsInPoints}
```
public Rectangle2D.Float getBoundsInPoints()
```


Şeklin gerçek sınırlarını nokta cinsinden alır.

 **Remarks:** 

Bu özellik, şeklin gerçek (sayfada render edildiği gibi) sınırlama kutusunu döndürür. Sınırlar, şekil dönüşünü (varsa) dikkate alır.

 **Examples:** 

Şekilleri ölçme ve ölçeklendirme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float - Şeklin nokta cinsinden gerçek sınırları.
### getOpaqueBoundsInPixels(float scale, float dpi) {#getOpaqueBoundsInPixels-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float dpi)
```


Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını piksel cinsinden hesaplar.

 **Remarks:** 

Bu yöntem [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) işlevini piksellerde bir dikdörtgene dönüştürür ve yalnızca şeklin opak kısmı ile render etmek için bir bitmap oluşturmak istediğinizde faydalıdır.

 **Examples:** 

Şekilleri ölçme ve ölçeklendirme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ölçek | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| dpi | float | Noktalardan piksellere (inç başına nokta) dönüştürme çözünürlüğü. |

**Returns:**
java.awt.Rectangle - Şeklin piksellerdeki opak dikdörtgeni.
### getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getOpaqueBoundsInPixels-float-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını piksel cinsinden hesaplar.

 **Remarks:** 

Bu yöntem [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) işlevini piksellerde bir dikdörtgene dönüştürür ve yalnızca şeklin opak kısmı ile render etmek için bir bitmap oluşturmak istediğinizde faydalıdır.

 **Examples:** 

Şekilleri ölçme ve ölçeklendirme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ölçek | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| horizontalDpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için yatay çözünürlük. |
| verticalDpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için dikey çözünürlük. |

**Returns:**
java.awt.Rectangle - Şeklin piksellerdeki opak dikdörtgeni.
### getOpaqueBoundsInPoints() {#getOpaqueBoundsInPoints}
```
public Rectangle2D.Float getOpaqueBoundsInPoints()
```


Şeklin opak sınırlarını nokta cinsinden alır.

 **Remarks:** 

Bu özellik, şeklin opak (yani şeklin şeffaf kısımları göz ardı edilir) sınırlama kutusunu döndürür. Sınırlar, şeklin dönüşünü dikkate alır.

 **Examples:** 

Şekilleri ölçme ve ölçeklendirme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float - Şeklin noktalardaki opak sınırları.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu piksel cinsinden hesaplar.

 **Remarks:** 

Bu yöntem [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) işlevini piksellerdeki boyuta dönüştürür ve şekli bitmap üzerine düzgün bir şekilde render etmek için bir bitmap oluşturmak istediğinizde faydalıdır.

 **Examples:** 

Şekilleri ölçme ve ölçeklendirme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ölçek | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| dpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için çözünürlük (yatay ve dikey). |

**Returns:**
java.awt.Dimension - Şeklin piksellerdeki boyutu.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu piksel cinsinden hesaplar.

 **Remarks:** 

Bu yöntem [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) işlevini piksellerdeki boyuta dönüştürür ve şekli bitmap üzerine düzgün bir şekilde render etmek için bir bitmap oluşturmak istediğinizde faydalıdır.

 **Examples:** 

Şekilleri ölçme ve ölçeklendirme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ölçek | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| horizontalDpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için yatay çözünürlük. |
| verticalDpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için dikey çözünürlük. |

**Returns:**
java.awt.Dimension - Şeklin piksellerdeki boyutu.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Şeklin gerçek boyutunu nokta cinsinden alır.

 **Remarks:** 

Bu özellik, şeklin gerçek (sayfada render edildiği gibi) sınırlama kutusunun boyutunu döndürür. Boyut, şeklin dönüşünü (varsa) dikkate alır.

 **Examples:** 

Şekilleri ölçme ve ölçeklendirme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Point2D.Float - Şeklin noktalardaki gerçek boyutu.
### renderToScale(Graphics2D graphics, float x, float y, float scale) {#renderToScale-java.awt.Graphics2D-float-float-float}
```
public Point2D.Float renderToScale(Graphics2D graphics, float x, float y, float scale)
```


Şekli belirtilen ölçeğe göre bir java.awt.Graphics2D nesnesine render eder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| grafikler | java.awt.Graphics2D | Render edilecek nesne. |
| x | float | Render edilen şeklin sol üst köşesinin X koordinatı (dünya birimlerinde). |
| y | float | Render edilen şeklin sol üst köşesinin Y koordinatı (dünya birimlerinde). |
| ölçek | float | Şekli render etmek için ölçek (1.0 = %100). |

**Returns:**
java.awt.geom.Point2D.Float - Render edilen şeklin genişlik ve yüksekliği (dünya birimlerinde).
### renderToSize(Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-java.awt.Graphics2D-float-float-float-float}
```
public float renderToSize(Graphics2D graphics, float x, float y, float width, float height)
```


Şekli belirtilen boyuta göre bir java.awt.Graphics2D nesnesine render eder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| grafikler | java.awt.Graphics2D | Render edilecek nesne. |
| x | float | Render edilen şeklin sol üst köşesinin X koordinatı (dünya birimlerinde). |
| y | float | Render edilen şeklin sol üst köşesinin Y koordinatı (dünya birimlerinde). |
| genişlik | float | Render edilen şeklin kaplayabileceği maksimum genişlik (dünya birimlerinde). |
| yükseklik | float | Render edilen şeklin kaplayabileceği maksimum yükseklik (dünya birimlerinde). |

**Returns:**
float - Belirtilen boyuta uyması için render edilen şekil için otomatik olarak hesaplanan ölçek.
### save(OutputStream stream, ImageSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions}
```
public void save(OutputStream stream, ImageSaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |

### save(OutputStream stream, SvgSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions}
```
public void save(OutputStream stream, SvgSaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) |  |

### save(String fileName, ImageSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public void save(String fileName, ImageSaveOptions saveOptions)
```


Şekli render eder ve bir görüntüye kaydeder. Şekli bir görüntüye render eder ve bir dosyaya kaydeder.

 **Examples:** 

Bir Office Math nesnesinin yerel dosya sistemindeki bir görüntü dosyasına nasıl render edileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);

 // Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
 // how it renders the OfficeMath node into an image.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "Scale" property to 5 to render the object to five times its original size.
 saveOptions.setScale(5f);

 math.getMathRenderer().save(getArtifactsDir() + "Shape.RenderOfficeMath.png", saveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Görüntü dosyasının adı. Belirtilen adla bir dosya zaten mevcutsa, mevcut dosya üzerine yazılır. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Şeklin nasıl işleneceğini ve kaydedileceğini kontrol eden seçenekleri belirtir. null olabilir. |

### save(String fileName, SvgSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SvgSaveOptions}
```
public void save(String fileName, SvgSaveOptions saveOptions)
```


Şekli işleyerek bir SVG görüntüsüne kaydeder.  Şekli bir SVG görüntüsüne işleyip bir dosyaya kaydeder.

 **Examples:** 

Office matematiği işlenirken kaydetme seçeneklerinin nasıl geçirileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath)doc.getChild(NodeType.OFFICE_MATH, 0, true);

 SvgSaveOptions options = new SvgSaveOptions();
 options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);

 math.getMathRenderer().save(getArtifactsDir() + "SvgSaveOptions.Output.svg", options);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Görüntü dosyasının adı. Belirtilen adla bir dosya zaten mevcutsa, mevcut dosya üzerine yazılır. |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) | Şeklin nasıl işleneceğini ve kaydedileceğini kontrol eden seçenekleri belirtir. null olabilir. |

