---
title: "Aspose::Words::Fields::FieldInclude::get_BookmarkName 方法"
linktitle: "get_BookmarkName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldInclude::get_BookmarkName 方法。获取或设置要在 C++ 中包含的文档书签的名称。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldinclude/get_bookmarkname/
---
## FieldInclude::get_BookmarkName method


获取或设置要包含的文档中书签的名称。

```cpp
System::String Aspose::Words::Fields::FieldInclude::get_BookmarkName() override
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
