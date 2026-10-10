---
title: "Aspose::Words::Fields::FieldIncludePicture class"
linktitle: "FieldIncludePicture"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIncludePicture class. 实现 INCLUDEPICTURE 字段。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 57000
url: /zh/cpp/aspose.words.fields/fieldincludepicture/
---
## FieldIncludePicture class


实现 INCLUDEPICTURE 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldIncludePicture : public Aspose::Words::Fields::Field,
                            public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                            public Aspose::Words::Fields::IFieldIncludePictureCode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_GraphicFilter](./get_graphicfilter/)() | 获取或设置要插入的图形格式的过滤器名称。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLinked](./get_islinked/)() override | 获取或设置是否通过不随文档存储图形数据来减小文件大小。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_ResizeHorizontally](./get_resizehorizontally/)() | 获取或设置是否水平调整来源图片的大小。 |
| [get_ResizeVertically](./get_resizevertically/)() | 获取或设置是否垂直调整来源图片的大小。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_SourceFullName](./get_sourcefullname/)() override | 获取或设置使用 IRI 的图片位置。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_GraphicFilter](./set_graphicfilter/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldIncludePicture::get_GraphicFilter](./get_graphicfilter/) 的 setter。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLinked](./set_islinked/)(bool) | 用于设置 [Aspose::Words::Fields::FieldIncludePicture::get_IsLinked](./get_islinked/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_ResizeHorizontally](./set_resizehorizontally/)(bool) | 用于设置 [Aspose::Words::Fields::FieldIncludePicture::get_ResizeHorizontally](./get_resizehorizontally/) 的 setter。 |
| [set_ResizeVertically](./set_resizevertically/)(bool) | 用于设置 [Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically](./get_resizevertically/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldIncludePicture::get_SourceFullName](./get_sourcefullname/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何使用 IMPORT 和 INCLUDEPICTURE 字段插入图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是两种相似的字段类型，可用于显示来自本地文件系统的链接图像。
// 1 -  INCLUDEPICTURE 字段：
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// 应用 PNG32.FLT 过滤器。
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  IMPORT 字段：
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
