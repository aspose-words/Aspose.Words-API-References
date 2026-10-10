---
title: "طريقة Aspose::Words::Document::RemoveCustomizations"
linktitle: "RemoveCustomizations"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::RemoveCustomizations. يزيل تخصيصات شريط الأدوات وأوامر لوحة المفاتيح من المستند في C++."
type: docs
weight: 67750
url: /ar/cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


يزيل تخصيصات شريط الأدوات وأوامر لوحة المفاتيح من المستند.

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## أمثلة



يعرض كيفية إزالة تخصيصات شريط الأدوات وأوامر لوحة المفاتيح من المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// إزالة جميع تخصيصات واجهة المستخدم للمستند، بما في ذلك إدخالات قائمة السياق المخصصة.
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
