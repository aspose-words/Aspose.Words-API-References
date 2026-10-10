---
title: "طريقة Aspose::Words::IDocumentConverterPlugin::Convert method"
linktitle: "تحويل"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::IDocumentConverterPlugin::Convert method. يحول المستند باستخدام تدفقات الإدخال والإخراج المحددة وخيارات الحفظ في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/idocumentconverterplugin/convert/
---
## IDocumentConverterPlugin::Convert method


يحوّل المستند باستخدام تدفقات الإدخال والإخراج المحددة وخيارات الحفظ.

```cpp
virtual void Aspose::Words::IDocumentConverterPlugin::Convert(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<System::IO::Stream> outputStream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | دفق الإدخال. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | خيارات تحميل المستند. |
| outputStream | System::SharedPtr\<System::IO::Stream\> | تدفق الإخراج. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | خيارات الحفظ. |

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
