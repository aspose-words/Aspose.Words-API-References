---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat method"
linktitle: "get_SaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat method. يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقط Text في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.saving/txtsaveoptions/get_saveformat/
---
## TxtSaveOptions::get_SaveFormat method


يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقط [Text](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat() override
```


## أمثلة



يظهر كيفية حفظ مستند .txt مع فاصل فقرة مخصص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل طريقة حفظ المستند كنص عادي.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// عيّن "ParagraphBreak" إلى قيمة مخصصة نرغب بوضعها في نهاية كل فقرة.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
