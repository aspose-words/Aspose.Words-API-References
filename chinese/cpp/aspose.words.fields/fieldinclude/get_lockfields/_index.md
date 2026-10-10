---
title: "Aspose::Words::Fields::FieldInclude::get_LockFields 方法"
linktitle: "get_LockFields"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldInclude::get_LockFields 方法。获取或设置是否阻止在 C++ 中更新包含文档中的字段。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fields/fieldinclude/get_lockfields/
---
## FieldInclude::get_LockFields method


获取或设置是否阻止包含文档中的字段被更新。

```cpp
bool Aspose::Words::Fields::FieldInclude::get_LockFields() override
```


## 示例



展示如何创建 INCLUDE 字段并设置其属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 我们可以使用 INCLUDE 字段从本地文件系统导入另一个文档的一部分。
// 我们通过此字段引用的另一个文档中的书签包含了此导入的部分。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## 另见

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
