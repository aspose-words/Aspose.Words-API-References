---
title: "Aspose::Words::Fields::FieldMergeBarcode 类"
linktitle: "FieldMergeBarcode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldMergeBarcode 类。实现 MERGEBARCODE 字段。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 66000
url: /zh/cpp/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class


实现 MERGEBARCODE 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldMergeBarcode : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IMergeFieldSurrogate
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | 获取是否为条码类型 NW7 和 CODE39 添加起始/停止字符。 |
| [get_BackgroundColor](./get_backgroundcolor/)() | 获取条码符号的背景颜色。有效值范围为 [0, 0xFFFFFF]。 |
| [get_BarcodeType](./get_barcodetype/)() | 获取条码类型（QR 等）。 |
| [get_BarcodeValue](./get_barcodevalue/)() | 获取条码值。 |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_DisplayText](./get_displaytext/)() | 获取是否在图像旁显示条码数据（文本）。 |
| [get_End](./get_end/)() override | 获取表示字段结束的节点。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | 获取 QR 码的错误纠正级别。有效值为 [0, 3]。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | 获取当校验位无效时是否修正它。 |
| [get_ForegroundColor](./get_foregroundcolor/)() | 获取条形码符号的前景色。有效值范围为 [0, 0xFFFFFF]。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_ScalingFactor](./get_scalingfactor/)() | 获取符号的缩放因子。该值以整数百分比表示，有效值为 [10, 1000]。 |
| [get_Separator](./get_separator/)() override | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](./get_start/)() override | 获取表示字段起始的节点。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_SymbolHeight](./get_symbolheight/)() | 获取符号的高度。单位为 TWIPS（1/1440 英寸）。 |
| [get_SymbolRotation](./get_symbolrotation/)() | 获取条形码符号的旋转。有效值为 [0, 3]。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | 设置是否为条形码类型 NW7 和 CODE39 添加起始/停止字符。 |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | 设置条形码符号的背景色。有效值范围为 [0, 0xFFFFFF]。 |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | 设置条形码类型（QR 等）。 |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | 设置条形码的值。 |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | 设置是否在图像旁显示条形码数据（文本）。 |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | 设置 QR 码的错误纠正级别。有效值为 [0, 3]。 |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | 设置是否在校验位无效时进行修正。 |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | 设置条形码符号的前景色。有效值范围为 [0, 0xFFFFFF]。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | 设置符号的缩放因子。该值以整数百分比表示，有效值为 [10, 1000]。 |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | 设置符号的高度。单位为 TWIPS（1/1440 英寸）。 |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | 设置条形码符号的旋转。有效值为 [0, 3]。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
