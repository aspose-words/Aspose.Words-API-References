---
title: "طريقة Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel"
linktitle: "get_CompressionLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel. يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هي Normal في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/ooxmlsaveoptions/get_compressionlevel/
---
## OoxmlSaveOptions::get_CompressionLevel method


يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هي [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel() const
```


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

## انظر أيضًا

* Enum [CompressionLevel](../../compressionlevel/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
