---
title: "طريقة Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing"
linktitle: "get_UseAntiAliasing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing. يحصل على قيمة أو يحددها لتحديد ما إذا كان سيتم استخدام مضاد التعرج في عملية العرض في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام مضاد التسنين في العرض أم لا.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## ملاحظات


القيمة الافتراضية هي **false**. عندما يتم تعيين هذه القيمة إلى **true** يُستخدم مضاد التعرج في العرض.

يُستخدم هذا الخاصية عندما يتم تصدير المستند إلى الصيغ التالية: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/). عندما يتم تصدير المستند إلى صيغ [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) أو [Mobi](../../../aspose.words/saveformat/) يُستخدم هذا الخيار للصور النقطية.

## أمثلة



يوضح كيفية تحسين جودة المستند المعروض باستخدام [SaveOptions](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## انظر أيضًا

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
