---
title: "Aspose::Words::Fields::FieldSet::get_BookmarkName 方法"
linktitle: "get_BookmarkName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSet::get_BookmarkName 方法。获取或设置书签的名称（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldset/get_bookmarkname/
---
## FieldSet::get_BookmarkName method


获取或设置书签的名称。

```cpp
System::String Aspose::Words::Fields::FieldSet::get_BookmarkName()
```


## 示例



展示如何使用 SET 字段创建书签文本，然后使用 REF 字段在文档中显示它。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用 SET 字段为书签文本命名。
// 此字段指的是 "bookmark"，而不是文本中出现的书签结构，而是一个已命名的变量。
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// 在 REF 字段中按名称引用该书签并显示其内容。
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## 另见

* Class [FieldSet](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
