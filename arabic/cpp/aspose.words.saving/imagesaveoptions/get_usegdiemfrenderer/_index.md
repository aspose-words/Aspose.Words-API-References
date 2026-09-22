---
title: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer"
linktitle: "get_UseGdiEmfRenderer"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer. يحصل على قيمة أو يحددها لتحديد ما إذا كان سيتم استخدام مُعالج GDI+ أو مُعالج ملفات الميتا Aspose.Words عند الحفظ إلى EMF في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام GDI+ أو مُعالج ملفات الميتا Aspose.Words عند الحفظ إلى EMF.

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## ملاحظات


إذا تم تعيينه إلى **true** يُستخدم مُعالج ملفات الميتا GDI+. أي أن المحتوى يُكتب إلى كائن رسومات GDI+ ويُحفظ في ملف الميتا.

إذا تم تعيينه إلى **false** يُستخدم مُعالج ملفات الميتا Aspose.Words. أي أن المحتوى يُكتب مباشرةً إلى صيغة ملف الميتا باستخدام Aspose.Words.

يُطبق فقط عند الحفظ إلى EMF.

يعمل حفظ GDI+ فقط على .NET.

القيمة الافتراضية هي **true**.

## أمثلة



يوضح كيفية اختيار مُعالج عند تحويل مستند إلى .emf.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// عند حفظ المستند كصورة EMF، يمكننا تمرير كائن SaveOptions لاختيار مُعالج للصورة.
// إذا قمنا بتعيين علامة "UseGdiEmfRenderer" إلى "true"، سيستخدم Aspose.Words مُعالج GDI+.
// إذا قمنا بتعيين العلم "UseGdiEmfRenderer" إلى "false"، فإن Aspose.Words سيستخدم مُعالج الميتافايل الخاص به.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## انظر أيضًا

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
