---
title: "Aspose::Words::Fields::BarcodeParameters 类"
linktitle: "BarcodeParameters"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::BarcodeParameters 类。用于将条码参数传递给 BarcodeGenerator 的容器类。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


用于传递给 BarcodeGenerator 的条码参数的容器类。要了解更多，请访问[Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/)文档文章。

```cpp
class BarcodeParameters : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | 是否为条码类型 NW7 和 CODE39 添加起始/停止字符。 |
| [get_BackgroundColor](./get_backgroundcolor/)() const | 条码背景颜色 (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | 条码类型。 |
| [get_BarcodeValue](./get_barcodevalue/)() const | 要编码的数据。 |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayText](./get_displaytext/)() const | 是否在图像旁显示条码数据（文本）。 |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | QR 码的错误纠正级别。有效值为 [0, 3]。 |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | 面向识别标记 (FIM) 的类型。 |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | 是否在校验位无效时进行修正。 |
| [get_ForegroundColor](./get_foregroundcolor/)() const | 条码前景颜色 (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | 是否 [PostalAddress](./get_postaladdress/) 是书签的名称。 |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | 是否 [PostalAddress](./get_postaladdress/) 是美国邮政地址。 |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | 条码邮政地址。 |
| [get_ScalingFactor](./get_scalingfactor/)() const | 符号的缩放因子。该值以整数百分比表示，有效值为 [10, 1000]。 |
| [get_SymbolHeight](./get_symbolheight/)() const | 条码图像高度（以 twips 为单位 - 1/1440 英寸） |
| [get_SymbolRotation](./get_symbolrotation/)() const | 条码符号的旋转。有效值为 [0, 3]。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | 是否为条码类型 NW7 和 CODE39 添加起始/停止字符。 |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | 条码背景颜色 (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | 条码类型。 |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | 要编码的数据。 |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | 是否在图像旁显示条码数据（文本）。 |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | QR 码的错误纠正级别。有效值为 [0, 3]。 |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | 面向识别标记 (FIM) 的类型。 |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | 是否在校验位无效时进行修正。 |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | 条码前景颜色 (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | 是否 [PostalAddress](./get_postaladdress/) 是书签的名称。 |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | 是否 [PostalAddress](./get_postaladdress/) 是美国邮政地址。 |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | 条码邮政地址。 |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | 符号的缩放因子。该值以整数百分比表示，有效值为 [10, 1000]。 |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | 条码图像高度（以 twips 为单位 - 1/1440 英寸） |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | 条码符号的旋转。有效值为 [0, 3]。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
