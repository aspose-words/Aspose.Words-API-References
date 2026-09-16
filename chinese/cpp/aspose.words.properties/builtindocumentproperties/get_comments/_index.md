---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments 方法"
linktitle: "get_Comments"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments 方法。获取或设置文档注释（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_comments/
---
## BuiltInDocumentProperties::get_Comments method


获取或设置文档的注释。

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments()
```


## 示例



展示如何在 “Description” 类别中使用内置文档属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// 下面列出四个内置文档属性，它们有字段可以在文档正文中显示其值。
// 1 -  “Author” 属性，可使用 AUTHOR 域显示：
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 -  “Title” 属性，可使用 TITLE 域显示：
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 -  “Subject” 属性，可使用 SUBJECT 域显示：
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 -  “Comments” 属性，可使用 COMMENTS 域显示：
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// 内置属性 “Category” 没有可显示其值的域。
properties->set_Category(u"My category");

// 我们可以通过使用分号分隔 “Keywords” 属性的字符串值，为文档设置多个关键字。
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// 我们可以在 Windows 资源管理器中右键单击此文档，在 “Properties” → “Details” 中找到这些属性。
// 内置属性 “Author” 位于 “Origin” 组，其他属性位于 “Description” 组。
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## 另见

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
