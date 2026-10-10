---
title: "Aspose::Words::DocumentBuilder::MoveToField method"
linktitle: "MoveToField"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::MoveToField 方法。将光标移动到文档中的字段（C++）。"
type: docs
weight: 56000
url: /zh/cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


将光标移动到文档中的字段。

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 字段 | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | 要将光标移动到的字段。 |
| isAfter | bool | 当 **true** 时，光标移动到字段结束之后。 当 **false** 时，光标移动到字段开始之前。 |

## 示例



展示如何将 DocumentBuilder 的节点插入点光标移动到特定字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用 DocumentBuilder 插入字段，并在其后添加一段文本。
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// 构建器的光标当前位于文档末尾。
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// 将光标移动到字段，同时指定将光标放在字段之前还是之后。
builder->MoveToField(field, moveCursorToAfterTheField);

// 请注意，在两种情况下光标都位于字段之外。
// 这意味着我们不能这样使用构建器编辑字段。
// 要编辑字段，我们可以在字段的 FieldStart 上使用构建器的 MoveTo 方法
// 或 FieldSeparator 节点将光标放置在内部。
if (moveCursorToAfterTheField)
{
    ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));
    builder->Write(u" Text immediately after the field.");

    ASSERT_EQ(u"\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", doc->GetText().Trim());
}
else
{
    ASPOSE_ASSERT_EQ(field->get_Start(), builder->get_CurrentNode());
    builder->Write(u"Text immediately before the field. ");

    ASSERT_EQ(u"Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", doc->GetText().Trim());
}
```

## 另见

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
