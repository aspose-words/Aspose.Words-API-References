---
title: "Aspose::Words::Fields::IBarcodeGenerator 接口"
linktitle: "IBarcodeGenerator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IBarcodeGenerator 接口。条形码自定义生成器的公共接口。实现应由用户在 C++ 中提供。"
type: docs
weight: 118000
url: /zh/cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


条形码自定义生成器的公共接口。实现应由用户提供。

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | 使用一组参数生成条形码图像（用于 DisplayBarcode 字段）。 |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | 使用一组参数生成条形码图像（用于传统的 Barcode 字段）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
