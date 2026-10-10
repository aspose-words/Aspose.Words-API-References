---
title: "طريقة Aspose::Words::Fields::FieldHyperlink::get_ScreenTip"
linktitle: "get_ScreenTip"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldHyperlink::get_ScreenTip. تحصل أو تعيين نص تلميح الشاشة للارتباط التشعبي في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fields/fieldhyperlink/get_screentip/
---
## FieldHyperlink::get_ScreenTip method


يحصل أو يعيّن نص تلميح الشاشة للارتباط التشعبي.

```cpp
System::String Aspose::Words::Fields::FieldHyperlink::get_ScreenTip()
```


## أمثلة



يعرض كيفية استخدام حقول HYPERLINK للربط بالمستندات في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// عند النقر على حقل HYPERLINK هذا في Microsoft Word،
// سيفتح المستند المرتبط ثم يضع المؤشر عند الإشارة المرجعية المحددة.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// عند النقر على حقل HYPERLINK هذا في Microsoft Word،
// سيفتح المستند المرتبط، ويقوم بالتمرير تلقائيًا إلى الإطار المضمن المحدد.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## انظر أيضًا

* Class [FieldHyperlink](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
