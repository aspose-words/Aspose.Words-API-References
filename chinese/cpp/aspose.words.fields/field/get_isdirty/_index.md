---
title: "Aspose::Words::Fields::Field::get_IsDirty 方法"
linktitle: "get_IsDirty"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::Field::get_IsDirty 方法。获取或设置由于对文档进行其他修改而导致字段的当前结果不再正确（已过时）的状态（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.fields/field/get_isdirty/
---
## Field::get_IsDirty method


获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。

```cpp
bool Aspose::Words::Fields::Field::get_IsDirty()
```


## 示例



展示如何使用特殊属性来更新字段结果。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 为文档的内置 \"Author\" 属性赋值，然后使用字段显示它。
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// 更新属性。字段仍然显示旧值。
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// 由于字段的值已过期，我们可以将其标记为 \"dirty\"。
// 此值将保持过期，直到我们使用 Field.Update() 方法手动更新字段。
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // 如果我们在未调用更新方法的情况下保存，
    // 字段将在输出文档中继续显示过期的值。
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // LoadOptions 对象具有更新所有字段的选项
    // 在加载文档时标记为 \"dirty\"。
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // 这样更新 dirty 字段会自动将其 \"IsDirty\" 标志设为 false。
    if (updateDirtyFields)
    {
        ASSERT_EQ(u"John & Jane Doe", field->get_Result());
        ASSERT_FALSE(field->get_IsDirty());
    }
    else
    {
        ASSERT_EQ(u"John Doe", field->get_Result());
        ASSERT_TRUE(field->get_IsDirty());
    }
}
```

## 另见

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
