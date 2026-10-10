---
title: "طريقة Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts"
linktitle: "get_EmbedTrueTypeFonts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts. تحدد ما إذا كان يجب تضمين خطوط TrueType في المستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هي false في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


يحدد ما إذا كان سيتم تضمين خطوط TrueType في المستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هي **false**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## ملاحظات


يتيح تضمين خطوط TrueType للآخرين عرض المستند بنفس الخطوط التي تم استخدامها لإنشائه، ولكن قد يزيد ذلك بشكل كبير من حجم المستند.

يعمل هذا الخيار فقط مع صيغ DOC و DOCX و RTF.

## أمثلة



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

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
