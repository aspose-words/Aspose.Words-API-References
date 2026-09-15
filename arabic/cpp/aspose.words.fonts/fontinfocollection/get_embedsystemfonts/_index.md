---
title: "طريقة Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts"
linktitle: "get_EmbedSystemFonts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts. تحدد ما إذا كان يجب تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هي false. يعمل هذا الخيار فقط عندما يتم تعيين خيار EmbedTrueTypeFonts إلى true في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


تحدد ما إذا كان يجب تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هي **false**. يعمل هذا الخيار فقط عندما يتم تعيين خيار [EmbedTrueTypeFonts](../get_embedtruetypefonts/) إلى **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## ملاحظات


تعيين هذه الخاصية إلى **true** يكون مفيدًا إذا كان المستخدم على نظام شرق آسيوي ويرغب في إنشاء مستند يمكن قراءته من قبل الآخرين الذين لا يمتلكون خطوطًا لتلك اللغة على نظامهم. على سبيل المثال، يمكن لمستخدم على نظام ياباني اختيار تضمين الخطوط في المستند بحيث يكون المستند الياباني قابلًا للقراءة على جميع الأنظمة.

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
