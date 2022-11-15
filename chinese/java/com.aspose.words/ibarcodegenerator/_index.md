---
title: IBarcodeGenerator
second_title: Aspose.Words for Java API 参考
description: 条形码自定义生成器的公共接口。
type: docs
weight: 632
url: /zh/java/com.aspose.words/ibarcodegenerator/
---
```
public interface IBarcodeGenerator
```

条形码自定义生成器的公共接口。实施应由用户提供。生成器实例应该通过[FieldOptions.getBarcodeGenerator()](../../com.aspose.words/fieldoptions\#getBarcodeGenerator--) / [FieldOptions.setBarcodeGenerator(com.aspose.words.IBarcodeGenerator)](../../com.aspose.words/fieldoptions\#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator-)财产。
## 方法

| 方法 | 描述 |
| --- | --- |
| [getBarcodeImage(Barcode参数 parameters)](#getBarcodeImage-com.aspose.words.Barcode参数-) | 使用参数集（对于 DisplayBarcode 字段）生成条形码图像。 |
| [getOldBarcodeImage(Barcode参数 parameters)](#getOldBarcodeImage-com.aspose.words.Barcode参数-) | 使用参数集生成条形码图像（用于老式 Barcode 字段）。 |
### getBarcodeImage(Barcode参数 parameters) {#getBarcodeImage-com.aspose.words.Barcode参数-}
```
public abstract BufferedImage getBarcodeImage(Barcode参数 parameters)
```


使用参数集（对于 DisplayBarcode 字段）生成条形码图像。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| parameters | [Barcode参数](../../com.aspose.words/barcodeparameters) | 参数集 |

**退货:**
java.awt.image.BufferedImage - 表示生成的条形码的图像。
### getOldBarcodeImage(Barcode参数 parameters) {#getOldBarcodeImage-com.aspose.words.Barcode参数-}
```
public abstract BufferedImage getOldBarcodeImage(Barcode参数 parameters)
```


使用参数集生成条形码图像（用于老式 Barcode 字段）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| parameters | [Barcode参数](../../com.aspose.words/barcodeparameters) | 参数集 |

**退货:**
java.awt.image.BufferedImage - 表示生成的条形码的图像。