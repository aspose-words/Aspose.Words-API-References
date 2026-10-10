---
title: "Aspose::Words::Fields::FieldRef::get_BookmarkName طريقة"
linktitle: "طريقة Aspose::Words::Fields::FieldAsk::set_DefaultResponse"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldRef::get_BookmarkName طريقة. يحصل أو يضبط اسم الإشارة المرجعية المشار إليها في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldref/get_bookmarkname/
---
## FieldRef::get_BookmarkName method


يحصل أو يعيّن اسم الإشارة المرجعية المشار إليها.

```cpp
System::String Aspose::Words::Fields::FieldRef::get_BookmarkName()
```


## أمثلة



يظهر كيفية إنشاء نص معلم باستخدام حقل SET، ثم عرضه في المستند باستخدام حقل REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// سمّ النص المعلم بحقل SET.
// يشير هذا الحقل إلى "bookmark" وليس إلى بنية علامة مرجعية تظهر داخل النص، بل إلى متغيّر مسمى.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// اشر إلى العلامة المرجعية بالاسم في حقل REF واعرض محتوياتها.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## انظر أيضًا

* Class [FieldRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
