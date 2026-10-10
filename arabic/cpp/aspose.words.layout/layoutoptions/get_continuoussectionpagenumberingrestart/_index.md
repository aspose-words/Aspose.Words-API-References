---
title: "طريقة Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart"
linktitle: "get_ContinuousSectionPageNumberingRestart"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart. يحصل أو يضبط وضع السلوك لحساب أرقام الصفحات عندما يعيد قسم متواصل ترقيم الصفحات في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


يحصل أو يعيّن وضع السلوك لحساب أرقام الصفحات عندما يعيد قسم متواصل ترقيم الصفحات.

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


## أمثلة



يظهر كيفية التحكم في ترقيم الصفحات في قسم مستمر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// بشكل افتراضي، سلوك Aspose.Words يطابق Microsoft Word 2019.
// إذا كنت بحاجة إلى سلوك Aspose.Words القديم، المتكرر في Microsoft Word 2016، استخدم 'ContinuousSectionRestart.FromNewPageOnly'.
// يُعاد بدء ترقيم الصفحات فقط إذا لم يكن هناك محتوى آخر قبل القسم على الصفحة التي يبدأ فيها القسم،
// وبسبب ذلك سيُعاد ضبط الترقيم إلى 2 بدءًا من الصفحة الثانية.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## انظر أيضًا

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
