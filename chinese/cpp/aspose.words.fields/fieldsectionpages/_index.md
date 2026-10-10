---
title: "Aspose::Words::Fields::FieldSectionPages 类"
linktitle: "FieldSectionPages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSectionPages 类。实现 SECTIONPAGES 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 89000
url: /zh/cpp/aspose.words.fields/fieldsectionpages/
---
## FieldSectionPages class


实现 SECTIONPAGES 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldSectionPages : public Aspose::Words::Fields::Field
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何使用 SECTION 和 SECTIONPAGES 字段按章节对页面进行编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// SECTION 字段显示其所在章节的编号。
builder->Write(u"Section ");
auto fieldSection = System::ExplicitCast<Aspose::Words::Fields::FieldSection>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSection, true));

ASSERT_EQ(u" SECTION ", fieldSection->GetFieldCode());

// PAGE 字段显示其所在页面的编号。
builder->Write(u"\nPage ");
auto fieldPage = System::ExplicitCast<Aspose::Words::Fields::FieldPage>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, true));

ASSERT_EQ(u" PAGE ", fieldPage->GetFieldCode());

// SECTIONPAGES 字段显示其所在章节跨越的页面数量。
builder->Write(u" of ");
auto fieldSectionPages = System::ExplicitCast<Aspose::Words::Fields::FieldSectionPages>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSectionPages, true));

ASSERT_EQ(u" SECTIONPAGES ", fieldSectionPages->GetFieldCode());

// 从页眉移出，返回主文档并插入两页。
// 所有这些页面都将在第一章节。我们的字段在每个页眉出现一次，
// 将为该章节的当前/总页数编号。
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 我们可以使用文档生成器这样插入一个新节。
// 这将影响所有后续页眉中 SECTION 和 SECTIONPAGES 字段显示的值。
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

// PAGE 字段将在整个文档中持续计数页码。
// 我们可以在每个节手动重置其计数，以按节跟踪页码。
builder->get_CurrentSection()->get_PageSetup()->set_RestartPageNumbering(true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SECTION.SECTIONPAGES.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
