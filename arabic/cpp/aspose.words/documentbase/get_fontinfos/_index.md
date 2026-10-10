---
title: "طريقة Aspose::Words::DocumentBase::get_FontInfos"
linktitle: "get_FontInfos"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBase::get_FontInfos. توفر إمكانية الوصول إلى خصائص الخطوط المستخدمة في هذا المستند في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


يوفر الوصول إلى خصائص الخطوط المستخدمة في هذا المستند.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## ملاحظات


يتم تحميل مجموعة تعريفات الخطوط هذه كما هي من المستند. قد تكون تعريفات [Font](../../font/) اختيارية أو مفقودة أو غير مكتملة في بعض المستندات.

لا تعتمد على هذه المجموعة لتأكيد أن خطًا معينًا مستخدم في المستند. يجب عليك فقط استخدام هذه المجموعة للحصول على معلومات حول الخطوط التي قد تُستخدم في المستند.

## أمثلة



يعرض كيفية طباعة تفاصيل الخطوط الموجودة في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// اطبع جميع الخطوط المستخدمة وغير المستخدمة في المستند.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


يوضح كيفية حفظ مستند مع خطوط TrueType المضمنة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## انظر أيضًا

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
