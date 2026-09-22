---
title: "طريقة Aspose::Words::Style::get_ParagraphFormat"
linktitle: "get_ParagraphFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Style::get_ParagraphFormat. تحصل على تنسيق الفقرة للنمط في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words/style/get_paragraphformat/
---
## Style::get_ParagraphFormat method


يحصل على تنسيق الفقرة للنمط.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::Style::get_ParagraphFormat()
```

## ملاحظات


بالنسبة إلى أنماط الأحرف والقوائم، تُعيد هذه الخاصية **null**.

## أمثلة



يظهر كيفية إنشاء واستخدام نمط فقرة مع تنسيق القائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء نمط فقرة مخصص.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// إنشاء قائمة والتأكد من أن الفقرات التي تستخدم هذا النمط ستستخدم هذه القائمة.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// تطبيق نمط الفقرة على الفقرة الحالية لمُنشئ المستند، ثم إضافة بعض النص.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// غيّر نمط مُنشئ المستند إلى نمط لا يحتوي على تنسيق القوائم واكتب فقرة أخرى.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../../paragraphformat/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
