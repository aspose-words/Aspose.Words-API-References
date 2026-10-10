---
title: "Aspose::Words::Fields::FieldHyperlink class"
linktitle: "FieldHyperlink"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldHyperlink class. 实现 HYPERLINK 字段。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 53000
url: /zh/cpp/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class


实现 HYPERLINK 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldHyperlink : public Aspose::Words::Fields::Field,
                       public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                       public Aspose::Words::Fields::IFieldResultFormatProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Address](./get_address/)() | 获取或设置此超链接跳转的位置。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsImageMap](./get_isimagemap/)() | 获取或设置是否向超链接追加坐标以用于服务器端图像映射。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_OpenInNewWindow](./get_openinnewwindow/)() | 获取或设置是否在新的浏览器窗口中打开目标站点。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_ScreenTip](./get_screentip/)() | 获取或设置超链接的屏幕提示文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_SubAddress](./get_subaddress/)() | 获取或设置文件中的位置，例如书签，此超链接将跳转到该位置。 |
| [get_Target](./get_target/)() | 获取或设置链接应重定向到的目标。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_Address](./set_address/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldHyperlink::get_Address](./get_address/) 的 setter。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsImageMap](./set_isimagemap/)(bool) | 用于设置 [Aspose::Words::Fields::FieldHyperlink::get_IsImageMap](./get_isimagemap/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_OpenInNewWindow](./set_openinnewwindow/)(bool) | 用于设置 [Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow](./get_openinnewwindow/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldHyperlink::get_ScreenTip](./get_screentip/) 的 setter。 |
| [set_SubAddress](./set_subaddress/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldHyperlink::get_SubAddress](./get_subaddress/) 的 setter。 |
| [set_Target](./set_target/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldHyperlink::get_Target](./get_target/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何使用 HYPERLINK 字段链接本地文件系统中的文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// 当我们在 Microsoft Word 中单击此 HYPERLINK 字段时，
// 它将打开链接的文档，然后将光标定位到指定的书签。
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// 当我们在 Microsoft Word 中单击此 HYPERLINK 字段时，
// 它将打开链接的文档，并自动滚动到指定的 iframe。
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
