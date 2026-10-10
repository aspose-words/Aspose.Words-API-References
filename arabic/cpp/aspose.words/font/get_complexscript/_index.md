---
title: "طريقة Aspose::Words::Font::get_ComplexScript"
linktitle: "get_ComplexScript"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_ComplexScript. تحدد ما إذا كان محتوى هذا المقطع سيُعامل كنص سكريبت معقد بغض النظر عن قيم أحرف Unicode الخاصة به عند تحديد تنسيق هذا المقطع في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words/font/get_complexscript/
---
## Font::get_ComplexScript method


يحدد ما إذا كان محتوى هذا المقطع سيُعامل كنص كتابة معقد بغض النظر عن قيم أحرف Unicode الخاصة به عند تحديد تنسيق هذا المقطع.

```cpp
bool Aspose::Words::Font::get_ComplexScript()
```


## أمثلة



يظهر كيفية إضافة نص يُعامل دائمًا كسكريبت معقد.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
