---
title: "Aspose::Words::Paragraph::AppendField 方法"
linktitle: "AppendField"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::AppendField 方法。在 C++ 中向此段落追加字段。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


向此段落追加字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | 要追加的字段类型。 |
| updateField | bool | 指定是否立即更新字段。 |

### ReturnValue

一个表示已追加字段的 [Field](../../../aspose.words.fields/field/) 对象。

## 示例



展示向段落追加字段的各种方式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// 以下是向段落末尾追加字段的三种方法。
// 1 -  使用字段类型追加 DATE 字段，然后更新它：
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  使用字段代码追加 TIME 字段：
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  使用字段代码追加 QUOTE 字段，并使其显示占位符值：
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// 此字段将在我们更新之前显示其占位符值。
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


向此段落追加字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | const System::String\& | 要追加的字段代码（不含大括号）。 |

### ReturnValue

一个表示已追加字段的 [Field](../../../aspose.words.fields/field/) 对象。

## 示例



展示向段落追加字段的各种方式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// 以下是向段落末尾追加字段的三种方法。
// 1 -  使用字段类型追加 DATE 字段，然后更新它：
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  使用字段代码追加 TIME 字段：
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  使用字段代码追加 QUOTE 字段，并使其显示占位符值：
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// 此字段将在我们更新之前显示其占位符值。
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


向此段落追加字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | const System::String\& | 要追加的字段代码（不含大括号）。 |
| fieldValue | const System::String\& | 要追加的字段值。对于没有值的字段，请传递 **null**。 |

### ReturnValue

一个表示已追加字段的 [Field](../../../aspose.words.fields/field/) 对象。

## 示例



展示向段落追加字段的各种方式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// 以下是向段落末尾追加字段的三种方法。
// 1 -  使用字段类型追加 DATE 字段，然后更新它：
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  使用字段代码追加 TIME 字段：
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  使用字段代码追加 QUOTE 字段，并使其显示占位符值：
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// 此字段将在我们更新之前显示其占位符值。
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
