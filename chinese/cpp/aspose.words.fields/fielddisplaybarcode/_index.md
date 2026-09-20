---
title: "Aspose::Words::Fields::FieldDisplayBarcode class"
linktitle: "FieldDisplayBarcode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldDisplayBarcode 类。实现 DISPLAYBARCODE 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 34000
url: /zh/cpp/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class


实现 DISPLAYBARCODE 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldDisplayBarcode : public Aspose::Words::Fields::Field,
                            public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | 获取或设置是否为条码类型 NW7 和 CODE39 添加起始/停止字符。 |
| [get_BackgroundColor](./get_backgroundcolor/)() | 获取或设置条码符号的背景颜色。有效值范围为 [0, 0xFFFFFF]。 |
| [get_BarcodeType](./get_barcodetype/)() | 获取或设置条码类型（如 QR 等）。 |
| [get_BarcodeValue](./get_barcodevalue/)() | 获取或设置条码值。 |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets or sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_DisplayText](./get_displaytext/)() | 获取或设置是否在图像旁显示条码数据（文本）。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | 获取或设置 QR 码的错误纠正级别。有效值为 [0, 3]。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | 获取或设置是否在校验位无效时进行修正。 |
| [get_ForegroundColor](./get_foregroundcolor/)() | 获取或设置条码符号的前景颜色。有效值范围为 [0, 0xFFFFFF]。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets or sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_ScalingFactor](./get_scalingfactor/)() | 获取或设置符号的缩放因子。该值为整数百分比，有效范围为 [10, 1000]。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_SymbolHeight](./get_symbolheight/)() | 获取或设置符号的高度。单位为 TWIPS（1/1440 英寸）。 |
| [get_SymbolRotation](./get_symbolrotation/)() | 获取或设置条码符号的旋转。有效值为 [0, 3]。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_AddStartStopChar](./get_addstartstopchar/) 的 setter。 |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_BackgroundColor](./get_backgroundcolor/) 的 setter。 |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeType](./get_barcodetype/) 的 setter。 |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeValue](./get_barcodevalue/) 的 setter。 |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_CaseCodeStyle](./get_casecodestyle/) 的 setter。 |
| [set_DisplayText](./set_displaytext/)(bool) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_DisplayText](./get_displaytext/)。 |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)。 |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_FixCheckDigit](./get_fixcheckdigit/)。 |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor](./get_foregroundcolor/)。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_PosCodeStyle](./get_poscodestyle/)。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_ScalingFactor](./get_scalingfactor/)。 |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolHeight](./get_symbolheight/)。 |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolRotation](./get_symbolrotation/)。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何插入 DISPLAYBARCODE 字段并设置其属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// 以下是四种条形码类型，采用不同方式装饰，DISPLAYBARCODE 字段可以显示它们。
// 1 -  自定义颜色的 QR 码：
field->set_BarcodeType(u"QR");
field->set_BarcodeValue(u"ABC123");
field->set_BackgroundColor(u"0xF8BD69");
field->set_ForegroundColor(u"0xB5413B");
field->set_ErrorCorrectionLevel(u"3");
field->set_ScalingFactor(u"250");
field->set_SymbolHeight(u"1000");
field->set_SymbolRotation(u"0");

ASSERT_EQ(u" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field->GetFieldCode());
builder->Writeln();

// 2 -  带有条码下方数字的 EAN13 条码：
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  CODE39 条码：
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  带有指定案例代码的 ITF4 条码：
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
