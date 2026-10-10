---
title: "Aspose::Words::Paragraph::InsertField 方法"
linktitle: "InsertField"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::InsertField 方法。向此段落插入字段（C++）。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


在此段落中插入字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | 要插入的字段类型。 |
| updateField | bool | 指定是否立即更新字段。 |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | 此段落内的参考节点（如果 *refNode* 为 **null**，则追加到段落末尾）。 |
| isAfter | bool | 是否在参考节点之后或之前插入字段。 |

### ReturnValue

一个表示已插入字段的 [Field](../../../aspose.words.fields/field/) 对象。

## 示例



展示向段落添加字段的各种方法。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// 以下是向段落插入字段的三种方法。
// 1 - 在段落的一个子节点之后插入 AUTHOR 字段：
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 - 在段落的一个子节点之后插入 QUOTE 字段：
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 - 在段落的一个子节点之前插入 QUOTE 字段，
// 并使其显示占位符值：
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// 此字段将在我们更新之前显示其占位符值。
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


在此段落中插入字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | const System::String\& | 要插入的字段代码（不含大括号）。 |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | 此段落内的参考节点（如果 *refNode* 为 **null**，则追加到段落末尾）。 |
| isAfter | bool | 是否在参考节点之后或之前插入字段。 |

### ReturnValue

一个表示已插入字段的 [Field](../../../aspose.words.fields/field/) 对象。

## 示例



展示向段落添加字段的各种方法。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// 以下是向段落插入字段的三种方法。
// 1 - 在段落的一个子节点之后插入 AUTHOR 字段：
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 - 在段落的一个子节点之后插入 QUOTE 字段：
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 - 在段落的一个子节点之前插入 QUOTE 字段，
// 并使其显示占位符值：
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// 此字段将在我们更新之前显示其占位符值。
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


在此段落中插入字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | const System::String\& | 要插入的字段代码（不含大括号）。 |
| fieldValue | const System::String\& | 要插入的字段值。对于没有值的字段，请传入 **null**。 |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | 此段落内的参考节点（如果 *refNode* 为 **null**，则追加到段落末尾）。 |
| isAfter | bool | 是否在参考节点之后或之前插入字段。 |

### ReturnValue

一个表示已插入字段的 [Field](../../../aspose.words.fields/field/) 对象。

## 示例



展示向段落添加字段的各种方法。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// 以下是向段落插入字段的三种方法。
// 1 - 在段落的一个子节点之后插入 AUTHOR 字段：
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 - 在段落的一个子节点之后插入 QUOTE 字段：
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 - 在段落的一个子节点之前插入 QUOTE 字段，
// 并使其显示占位符值：
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// 此字段将在我们更新之前显示其占位符值。
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
