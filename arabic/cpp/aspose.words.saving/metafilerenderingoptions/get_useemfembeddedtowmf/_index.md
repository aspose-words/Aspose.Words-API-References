---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method"
linktitle: "get_UseEmfEmbeddedToWmf"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method. يحصل أو يحدد قيمة تحدد كيفية عرض ملفات WMF التي تحتوي على ملفات EMF مدمجة في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


يحصل أو يعيّن قيمة تحدد كيفية تصيير ملفات WMF التي تحتوي على ملفات EMF مدمجة.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## ملاحظات


قد تحتوي ملفات WMF على بيانات EMF مدمجة. يستخدم MS Word في معظم الحالات بيانات EMF المدمجة. يستخدم GDI+ دائمًا بيانات WMF.

عند تعيين هذه القيمة إلى **true**، يستخدم Aspose.Words بيانات EMF المدمجة عند التصيير.

عند تعيين هذه القيمة إلى **false**، يستخدم Aspose.Words بيانات WMF عند التصيير.

يُستخدم هذا الخيار فقط عندما يتم تصيير ملف الميتا كرسومات متجهة. عندما يتم تصيير ملف الميتا إلى صورة نقطية، تُستخدم بيانات WMF دائمًا.

القيمة الافتراضية هي **true**.
## انظر أيضًا

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
