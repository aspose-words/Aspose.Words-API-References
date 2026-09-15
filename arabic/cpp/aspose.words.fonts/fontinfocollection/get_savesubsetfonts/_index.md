---
title: "طريقة Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts"
linktitle: "get_SaveSubsetFonts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts. تحدد ما إذا كان سيتم حفظ مجموعة فرعية من خطوط TrueType المدمجة مع المستند أم لا. القيمة الافتراضية لهذه الخاصية هي false. يعمل هذا الخيار فقط عندما تكون خاصية EmbedTrueTypeFonts مضبوطة على true في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


تحدد ما إذا كان سيتم حفظ مجموعة فرعية من خطوط TrueType المدمجة مع المستند أم لا. القيمة الافتراضية لهذه الخاصية هي **false**. يعمل هذا الخيار فقط عندما تكون خاصية [EmbedTrueTypeFonts](../get_embedtruetypefonts/) مضبوطة على **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


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
