---
title: "Aspose::Words::DocumentBuilder::InsertField 方法"
linktitle: "InsertField"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertField 方法。将 Word 字段插入文档，并可选择在 C++ 中更新字段结果。"
type: docs
weight: 34000
url: /zh/cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType, bool) method


将 Word 字段插入文档，并可选择性更新字段结果。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | 要追加的字段类型。 |
| updateField | bool | 指定是否立即更新字段。 |

### ReturnValue

一个表示已插入字段的 [Field](../../../aspose.words.fields/field/) 对象。
## 备注


此方法将在文档中插入字段。Aspose.Words 可以更新大多数类型的字段，但并非全部。更多详情请参阅 [InsertField()](../) 重载。

## 示例



展示如何使用 FieldType 将字段插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在插入两个字段时传递一个标志，以决定构建器插入时是否更新它们。
// 在某些情况下，更新字段可能计算成本高，最好延迟更新。
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(u" AUTHOR ", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
ASSERT_EQ(u" PAGE ", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
else
{
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

    // 我们需要手动使用更新方法来更新这些字段。
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&) method


将 Word 字段插入文档并更新字段结果。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | const System::String\& | 要插入的字段代码（不含大括号）。 |

### ReturnValue

一个表示已插入字段的 [Field](../../../aspose.words.fields/field/) 对象。
## 备注


此方法将在文档中插入字段并立即更新字段结果。Aspose.Words 可以更新大多数类型的字段，但并非全部。更多详情请参阅 [InsertField()](../) 重载。

## 示例



展示如何插入字段并将文档构建器的光标移动到这些字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// 将光标移动到第一个 MERGEFIELD。
builder->MoveToMergeField(u"MyMergeField1", true, false);

// 请注意，光标位于第一个 MERGEFIELD 之后、第二个之前。
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// 如果我们希望使用构建器编辑字段的字段代码或内容，
// 光标需要位于字段内部。
// 要将光标放入字段内部，需要调用文档构建器的 MoveTo 方法
// 并将字段的起始节点或分隔节点作为参数传入。
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```


展示如何使用字段代码向文档插入字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// 此 InsertField 方法的重载会自动更新插入的字段。
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&, const System::String\&) method


将 Word 字段插入文档但不更新字段结果。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | const System::String\& | 要插入的字段代码（不含大括号）。 |
| fieldValue | const System::String\& | 要插入的字段值。对于没有值的字段，请传入 **null**。 |

### ReturnValue

一个表示已插入字段的 [Field](../../../aspose.words.fields/field/) 对象。
## 备注


[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

您可以在 Microsoft Word 中使用快捷键 Alt+F9 在显示字段代码和结果之间切换。字段代码显示在大括号 ( { } ) 之间。

要创建字段，您需要指定字段类型、字段代码和一个 \"placeholder\" 字段值。如果您不确定特定字段代码的语法，请先在 Microsoft Word 中创建该字段，然后切换以查看其字段代码。

Aspose.Words 可以计算大多数字段类型的字段结果，但此方法不会自动更新字段结果。由于字段结果不会自动计算，您需要传入一些字符串值（甚至是空字符串），这些值将被插入到字段结果中。该值将在字段更新之前作为占位符保留在字段结果中。要更新字段结果，您可以调用 [Update](../../../aspose.words.fields/field/update/) 在返回给您的字段对象上，或调用 [UpdateFields](../../document/updatefields/) 来更新整个文档中的字段。

## 示例



展示如何在章节中设置页码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// 将文档构建器移动到第一章节的主页眉，
// 该章节的每一页都会显示此页眉。
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// 插入一个 PAGE 域，它将显示当前页的页码。
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// 配置章节，使 PAGE 域显示的页码从 5 开始计数。
// 此外，配置所有 PAGE 域使用大写罗马数字显示页码。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// 为第二章节创建另一个主页眉，并包含另一个 PAGE 域。
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// 配置章节，使 PAGE 域显示的页码从 10 开始计数。
// 此外，配置所有 PAGE 域使用阿拉伯数字显示页码。
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
