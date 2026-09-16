---
title: "Aspose::Words::DocumentBuilder::MoveToMergeField 方法"
linktitle: "MoveToMergeField"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::MoveToMergeField 方法。将光标移动到指定合并字段之后的位置，并在 C++ 中删除该合并字段。"
type: docs
weight: 58000
url: /zh/cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


将光标移动到指定合并域之后的位置，并删除该合并域。

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldName | const System::String\& | 邮件合并字段的大小写不敏感名称。 |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## 备注


请注意，此方法在移动光标后会从文档中删除合并字段。

## 示例



展示如何使用 DocumentBuilder 填充 MERGEFIELD，而不是使用邮件合并。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一些 MERGEFIELD，这些字段在邮件合并期间接受来自数据源中同名列的数据，
// 然后手动填充它们。
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


将合并域移动到指定的合并域。

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldName | const System::String\& | 邮件合并字段的大小写不敏感名称。 |
| isAfter | bool | 当 **true** 时，光标移动到字段结束之后。 当 **false** 时，光标移动到字段开始之前。 |
| isDeleteField | bool | 当 **true** 时，删除合并字段。 |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

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

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
