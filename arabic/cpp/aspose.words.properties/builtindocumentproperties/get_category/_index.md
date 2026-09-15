---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Category method"
linktitle: "get_Category"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_Category. تحصل أو تعين فئة المستند في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_category/
---
## BuiltInDocumentProperties::get_Category method


يحصل أو يضبط فئة المستند.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Category()
```


## أمثلة



يعرض كيفية العمل مع خصائص المستند المدمجة في فئة \"Description\".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// فيما يلي أربع خصائص مستند مدمجة تحتوي على حقول يمكنها عرض قيمها في جسم المستند.
// 1 - خاصية "Author"، والتي يمكننا عرضها باستخدام حقل AUTHOR:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 - خاصية "Title"، والتي يمكننا عرضها باستخدام حقل TITLE:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 - خاصية "Subject"، والتي يمكننا عرضها باستخدام حقل SUBJECT:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 - خاصية "Comments"، والتي يمكننا عرضها باستخدام حقل COMMENTS:
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// خاصية "Category" المدمجة لا تحتوي على حقل يمكنه عرض قيمتها.
properties->set_Category(u"My category");

// يمكننا تعيين عدة كلمات مفتاحية لمستند عن طريق فصل قيمة السلسلة لخاصية "Keywords" باستخدام الفواصل المنقوطة.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// يمكننا النقر بزر الماوس الأيمن على هذا المستند في Windows Explorer والعثور على هذه الخصائص في "Properties" -> "Details".
// خاصية "Author" المدمجة موجودة في مجموعة "Origin"، والخصائص الأخرى في مجموعة "Description".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## انظر أيضًا

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
