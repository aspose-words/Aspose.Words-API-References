---
title: "طريقة Aspose::Words::Font::get_Spacing"
linktitle: "get_Spacing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_Spacing. تُرجع أو تضبط التباعد (بالنقاط) بين الأحرف في C++."
type: docs
weight: 40000
url: /ar/cpp/aspose.words/font/get_spacing/
---
## Font::get_Spacing method


إرجاع أو تعيين التباعد (بالنقاط) بين الأحرف.

```cpp
double Aspose::Words::Font::get_Spacing()
```


## أمثلة



يظهر كيفية ضبط مقياس الأفقية والمسافة بين الأحرف.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف مقطع نصي وزد عرض الأحرف إلى 150٪.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// أضف مقطع نصي وأضف 1pt من المسافة الأفقية الإضافية بين كل حرف.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// أضف مقطع نصي واقرب الأحرف من بعضها البعض بمقدار 1pt.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
