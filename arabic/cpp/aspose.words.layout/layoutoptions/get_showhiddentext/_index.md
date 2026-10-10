---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText طريقة"
linktitle: "get_ShowHiddenText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText طريقة. يحصل أو يضبط إشارة إلى ما إذا كان النص المخفي في المستند يُعرض. القيمة الافتراضية هي false في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


يحصل أو يعيّن إشارة ما إذا كان النص المخفي في المستند يتم عرضه. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## أمثلة



يظهر كيفية إخفاء النص في مستند الإخراج المرسوم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج نصًا مخفيًا، ثم حدد ما إذا كنا نرغب في حذفه من المستند المرسوم.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```

## انظر أيضًا

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
