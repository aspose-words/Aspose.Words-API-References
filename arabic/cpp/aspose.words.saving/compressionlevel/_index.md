---
title: "Aspose::Words::Saving::CompressionLevel enum"
linktitle: "CompressionLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::CompressionLevel enum. مستوى الضغط لملفات OOXML و XPS. (ملفات DOCX و DOTX و XPS هي داخليًا أرشيف ZIP، هذه الخاصية تتحكم في مستوى ضغط الأرشيف. لاحظ أن ملف FlatOpc ليس أرشيف ZIP، وبالتالي لا تؤثر هذه الخاصية على ملفات FlatOpc.) في C++."
type: docs
weight: 47000
url: /ar/cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


مستوى الضغط لملفات OOXML و XPS. (ملفات DOCX و DOTX و XPS هي داخليًا أرشيف ZIP، تتحكم هذه الخاصية في مستوى ضغط الأرشيف. لاحظ أن ملف FlatOpc ليس أرشيف ZIP، وبالتالي لا تؤثر هذه الخاصية على ملفات FlatOpc.)

```cpp
enum class CompressionLevel
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Normal | 0 | مستوى ضغط عادي. مستوى الضغط الافتراضي المستخدم بواسطة [Aspose.Words](../../aspose.words/). |
| الأقصى | 1 | أقصى مستوى ضغط. |
| سريع | 2 | مستوى ضغط سريع. |
| SuperFast | 3 | مستوى ضغط فائق السرعة. يستخدم Microsoft Word هذا المستوى من الضغط. |


## أمثلة



يوضح كيفية تحديد مستوى الضغط لاستخدامه أثناء حفظ مستند OOXML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// عند حفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم نمرره إلى طريقة حفظ المستند لتعديل طريقة حفظ المستند.
// قم بتعيين خاصية "CompressionLevel" إلى "CompressionLevel.Maximum" لتطبيق أقوى وأبطأ ضغط.
// قم بتعيين خاصية "CompressionLevel" إلى "CompressionLevel.Normal" لتطبيق
// الضغط الافتراضي الذي يستخدمه Aspose.Words أثناء حفظ مستندات OOXML.
// قم بتعيين خاصية "CompressionLevel" إلى "CompressionLevel.Fast" لتطبيق ضغط أسرع وأضعف.
// قم بتعيين خاصية "CompressionLevel" إلى "CompressionLevel.SuperFast" لتطبيق
// الضغط الافتراضي الذي يستخدمه Microsoft Word.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_CompressionLevel(compressionLevel);

System::SharedPtr<System::Diagnostics::Stopwatch> st = System::Diagnostics::Stopwatch::StartNew();
doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st->Stop();

auto fileInfo = System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"OoxmlSaveOptions.DocumentCompression.docx");

std::cout << System::String::Format(u"Saving operation done using the \"{0}\" compression level:", compressionLevel) << std::endl;
std::cout << System::String::Format(u"\tDuration:\t{0} ms", st->get_ElapsedMilliseconds()) << std::endl;
std::cout << System::String::Format(u"\tFile Size:\t{0} bytes", fileInfo->get_Length()) << std::endl;
```


يظهر كيفية التحكم في مستوى الضغط عند حفظ مستند إلى تنسيق XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// أنشئ كائن XpsSaveOptions وحدد مستوى الضغط.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
