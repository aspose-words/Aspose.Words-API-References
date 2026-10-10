---
title: "طريقة Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts"
linktitle: "get_AllowEmbeddingPostScriptFonts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts. يحصل على قيمة منطقية أو يحددها لتحديد ما إذا كان يُسمح بدمج الخطوط ذات المخططات PostScript عند دمج خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي false في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يُسمح بدمج الخطوط ذات المخططات PostScript عند دمج خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## ملاحظات


ملاحظة، لا يقوم Word بدمج خطوط PostScript، لكنه يمكنه فتح المستندات التي تحتوي على خطوط مدمجة من هذا النوع.

يعمل هذا الخيار فقط عندما يتم تعيين الخاصية [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) من خاصية [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) إلى **true**.

## أمثلة



يوضح كيفية حفظ المستند باستخدام خط PostScript.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// حمّل الخط بنظام PostScript لاستخدامه في المستند.
auto otf = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(System::IO::File::ReadAllBytes(get_FontsDir() + u"AllegroOpen.otf"));
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({otf}));

// دمج خطوط TrueType.
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// السماح بدمج خطوط PostScript أثناء دمج خطوط TrueType.
// Microsoft Word لا يدمج خطوط PostScript، لكنه يمكنه فتح المستندات التي تحتوي على خطوط مدمجة من هذا النوع.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(get_ArtifactsDir() + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## انظر أيضًا

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
