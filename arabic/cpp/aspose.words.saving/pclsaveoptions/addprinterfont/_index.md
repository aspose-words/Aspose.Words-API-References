---
title: "طريقة Aspose::Words::Saving::PclSaveOptions::AddPrinterFont"
linktitle: "AddPrinterFont"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PclSaveOptions::AddPrinterFont. تُضيف معلومات حول الخط الذي يتم تحميله إلى الطابعة من قبل الشركة المصنعة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions::AddPrinterFont method


يضيف معلومات حول الخط الذي يتم تحميله إلى الطابعة من قبل الشركة المصنعة.

```cpp
void Aspose::Words::Saving::PclSaveOptions::AddPrinterFont(const System::String &fontFullName, const System::String &fontPclName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fontFullName | const System::String\& | الاسم الكامل للخط (مثال: "Times New Roman Bold Italic"). |
| fontPclName | const System::String\& | اسم الخط المستخدم في مستند Pcl. |

## أمثلة



يوضح كيفية جعل الطابعة تستبدل جميع حالات خط معين بخط مختلف.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Courier");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->AddPrinterFont(u"Courier New", u"Courier");

// عند طباعة هذا المستند، ستستخدم الطابعة الخط "Courier New"
// للوصول إلى الأماكن التي استخدم فيها مستندنا الخط "Courier".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

## انظر أيضًا

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
