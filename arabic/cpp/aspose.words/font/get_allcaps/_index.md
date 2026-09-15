---
title: "طريقة Aspose::Words::Font::get_AllCaps"
linktitle: "get_AllCaps"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_AllCaps. صحيح إذا كان الخط مُنسقًا بأحرف كبيرة بالكامل في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/font/get_allcaps/
---
## Font::get_AllCaps method


صحيح إذا كان الخط مُنسقًا كحروف كبيرة كلها.

```cpp
bool Aspose::Words::Font::get_AllCaps()
```


## أمثلة



يظهر كيفية تنسيق مقطع لعرض محتوياته بأحرف كبيرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// هناك طريقتان لجعل مقطع يعرض نصه الصغير بأحرف كبيرة دون تغيير المحتوى.
// 1 -  اضبط علامة AllCaps لعرض جميع الأحرف بأحرف كبيرة عادية:
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

// 2 -  اضبط علامة SmallCaps لعرض جميع الأحرف بأحرف صغيرة كبيرة:
// إذا كان الحرف صغيرًا، سيظهر بصورته الكبيرة
// لكن سيبقى بنفس ارتفاع الحرف الصغير (ارتفاع x للخط).
// الأحرف التي كانت كبيرة أصلاً ستظهر كما هي.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.Caps.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
