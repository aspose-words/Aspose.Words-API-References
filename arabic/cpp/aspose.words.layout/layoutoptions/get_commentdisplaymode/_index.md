---
title: "طريقة Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode"
linktitle: "get_CommentDisplayMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode. يحصل أو يعيّن طريقة عرض التعليقات. القيمة الافتراضية هي ShowInBalloons في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.layout/layoutoptions/get_commentdisplaymode/
---
## LayoutOptions::get_CommentDisplayMode method


يحصل أو يعيّن طريقة عرض التعليقات. القيمة الافتراضية هي [ShowInBalloons](../../commentdisplaymode/).

```cpp
Aspose::Words::Layout::CommentDisplayMode Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode() const
```


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

* Enum [CommentDisplayMode](../../commentdisplaymode/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
