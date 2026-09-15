---
title: "Aspose::Words::Layout::ContinuousSectionRestart enum"
linktitle: "ContinuousSectionRestart"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::ContinuousSectionRestart enum. يمثل سلوكيات مختلفة عند حساب أرقام الصفحات في قسم مستمر يعيد بدء ترقيم الصفحات في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


يمثل سلوكيات مختلفة عند حساب أرقام الصفحات في قسم مستمر يعيد بدء ترقيم الصفحات.

```cpp
enum class ContinuousSectionRestart
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| دائمًا | 0 | يُعاد دائمًا بدء ترقيم الصفحات بغض النظر عن تدفق المحتوى. |
| FromNewPageOnly | 1 | يُعاد بدء ترقيم الصفحات فقط إذا لم يكن هناك محتوى آخر قبل القسم على الصفحة التي يبدأ فيها القسم. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
