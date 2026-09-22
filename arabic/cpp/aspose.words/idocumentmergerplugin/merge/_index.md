---
title: "طريقة Aspose::Words::IDocumentMergerPlugin::Merge"
linktitle: "دمج"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::IDocumentMergerPlugin::Merge. يدمج مستندات PDF المدخلة المعطاة في مستند PDF واحد ناتج باستخدام تدفقات الإدخال والإخراج المحددة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/idocumentmergerplugin/merge/
---
## IDocumentMergerPlugin::Merge method


يقوم بدمج مستندات PDF المدخلة المعطاة في مستند PDF واحد كخرج باستخدام تدفقات الإدخال والإخراج المحددة.

```cpp
virtual void Aspose::Words::IDocumentMergerPlugin::Merge(System::SharedPtr<System::IO::Stream> outputStream, System::ArrayPtr<System::SharedPtr<System::IO::Stream>> inputStreams, System::ArrayPtr<System::SharedPtr<Aspose::Words::Loading::LoadOptions>> loadOptions)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | تدفق الإخراج. |
| inputStreams | System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\> | تدفقات الإدخال. |
| loadOptions | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\> | خيارات التحميل للملفات المدخلة. |

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Interface [IDocumentMergerPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
