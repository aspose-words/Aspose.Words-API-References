---
title: "طريقة Aspose::Words::IDocumentReaderPlugin::Read"
linktitle: "قراءة"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::IDocumentReaderPlugin::Read. تقرأ البيانات من الدفق المحدد إلى كائن Document في لغة C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin::Read method


تقرأ البيانات من الدفق المحدد إلى كائن [Document](../../document/).

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | دفق المصدر لقراءة المستند منه. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | خيارات تحميل إضافية لتحميل المستند. |
| document | System::SharedPtr\<Aspose::Words::Document\> | مثيل فئة [Document](../../document/) لقراءة البيانات إليه. إذا كان المثيل يحتوي على بعض المحتوى، فسيتم استبداله بالبيانات من دفق المصدر. |

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../../document/)
* Interface [IDocumentReaderPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
