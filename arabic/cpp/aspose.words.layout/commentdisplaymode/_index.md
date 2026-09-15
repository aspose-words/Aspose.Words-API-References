---
title: "Aspose::Words::Layout::CommentDisplayMode enum"
linktitle: "CommentDisplayMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::CommentDisplayMode enum. يحدد وضعية العرض لتعليقات المستند في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


يحدد وضعية العرض لتعليقات المستند.

```cpp
enum class CommentDisplayMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Hide | 0 | لا يتم عرض أي تعليقات على المستند. |
| ShowInBalloons | 1 | يعرض تعليقات المستند في فقاعات على الهامش. هذه هي القيمة الافتراضية. |
| ShowInAnnotations | 2 | يعرض تعليقات المستند في التعليقات التوضيحية. هذا متاح فقط لتنسيق Pdf. |


## أمثلة



يوضح كيفية إظهار التعليقات عند حفظ المستند بتنسيق معروض.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations متاح فقط في تنسيقي Pdf1.7 وPdf1.5.
// في التنسيقات الأخرى، سيعمل بطريقة مماثلة لـ Hide.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// لاحظ أنه من الضروري إعادة بناء تخطيط صفحات المستند (عن طريق طريقة Document.UpdatePageLayout()).
// بعد تغيير قيم Document.LayoutOptions.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## انظر أيضًا

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
