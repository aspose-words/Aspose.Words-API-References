---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method"
linktitle: "get_FontResourcesSubsettingSizeThreshold"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method. يتحكم في أي موارد الخط تحتاج إلى تقليص عند الحفظ إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي %0 في C++."
type: docs
weight: 31000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


يتحكم في أي موارد الخط تحتاج إلى تقليص عند الحفظ إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **%0**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## ملاحظات


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## أمثلة



يوضح كيفية العمل مع تقليل حجم الخط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions لتكوين تقليل حجم الخط.
// افترض أننا قمنا بتعيين العلامة "ExportFontResources" إلى "true" وأيضًا حددنا مجلدًا في الخاصية "FontsFolder".
// في هذه الحالة، ستقوم عملية الحفظ بإنشاء ذلك المجلد ووضع ملف .ttf داخله
// ذلك المجلد لكل خط يستخدمه مستندنا.
// كل ملف .ttf سيحتوي على مجموعة الرموز الكاملة لذلك الخط،
// مما قد يؤدي إلى ملف كبير جدًا يرافق المستند.
// عند تطبيق تقليل الحجم على خط، ستحتوي البيانات الخام المصدرة له فقط على الرموز التي يكون المستند
// يستخدمها بدلاً من مجموعة الرموز الكاملة. إذا كان النص في مستندنا يستخدم فقط جزءًا صغيرًا من
// مجموعة الرموز، فإن تقليل الحجم سيقلل بشكل كبير من حجم المستندات الناتجة.
// يمكننا استخدام الخاصية "FontResourcesSubsettingSizeThreshold" لتحديد حجم ملف .ttf، بالبايت.
// إذا أنشأ خط مُصدَّر ملفًا أكبر حجمًا من ذلك، فستقوم عملية الحفظ بتطبيق تقليل الحجم على ذلك الخط.
// تعيين حد بقيمة 0 يطبق تقليل الحجم على جميع الخطوط،
// وضعه على "int.MaxValue" يعطل التجزئة فعليًا.
System::String fontsFolder = get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.Fonts";

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontResources(true);
options->set_FontsFolder(fontsFolder);
options->set_FontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.html", options);

System::ArrayPtr<System::String> fontFileNames = System::IO::Directory::GetFiles(fontsFolder)->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String s)>>([](System::String s) -> bool
{
    return s.EndsWith(u".ttf");
})))->LINQ_ToArray();

ASSERT_EQ(3, fontFileNames->get_Length());

for (System::String filename : fontFileNames)
{
    // بشكل افتراضي، ملفات .ttf لكل من خطوطنا الثلاثة ستكون أكثر من 700 ميغابايت.
    // ستقلل التجزئة جميعها إلى أقل من 30 ميغابايت.
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
