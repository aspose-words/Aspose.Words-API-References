---
title: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages طريقة"
linktitle: "ConvertToImages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages method. يحول الصفحات من المستند من تدفق الإدخال إلى مصفوفة من الصور في C++."
type: docs
weight: 2500
url: /ar/cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


يحوّل الصفحات من المستند من تدفق الإدخال إلى مصفوفة من الصور.

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | دفق الإدخال. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | خيارات تحميل المستند. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | خيارات الحفظ. |

### ReturnValue

مصفوفة من تدفقات صور الصفحات.

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
