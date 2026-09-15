---
title: "طريقة Aspose::Words::Paragraph::GetEffectiveTabStops"
linktitle: "GetEffectiveTabStops"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Paragraph::GetEffectiveTabStops. تُرجع مصفوفة جميع نقاط التبويب المطبقة على هذه الفقرة، بما في ذلك تلك المطبقة بشكل غير مباشر عبر الأنماط أو القوائم في C++."
type: docs
weight: 26000
url: /ar/cpp/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph::GetEffectiveTabStops method


يرجع مصفوفة جميع نقاط التبويب المطبقة على هذه الفقرة، بما في ذلك تلك المطبقة بشكل غير مباشر عبر الأنماط أو القوائم.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::TabStop>> Aspose::Words::Paragraph::GetEffectiveTabStops()
```


## أمثلة



يوضح كيفية تعيين مواضع تبويب مخصصة لفقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// إذا كنا في فقرة لا تحتوي على مواضع تبويب في هذه المجموعة،
// سوف يقفز المؤشر 36 نقطة في كل مرة نضغط فيها على مفتاح Tab في Microsoft Word.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// يمكننا إضافة مواضع تبويب مخصصة في Microsoft Word إذا فعلنا المسطرة عبر علامة تبويب "View".
// كل وحدة على هذه المسطرة تمثل موضعين تبويب افتراضيين، أي 72 نقطة.
// يمكننا إضافة مواضع تبويب مخصصة برمجيًا بهذه الطريقة.
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// يمكننا رؤية هذه مواضع التبويب في Microsoft Word عن طريق تفعيل المسطرة عبر "View" -> "Show" -> "Ruler".
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// أي أحرف تبويب نضيفها ستستخدم مواضع التبويب على المسطرة وقد،
// اعتمادًا على قيمة قائد التبويب، تترك خطًا بين نقطة بدء التبويب ونقطة وصوله.
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## انظر أيضًا

* Class [TabStop](../../tabstop/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
