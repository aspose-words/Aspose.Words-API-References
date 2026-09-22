---
title: "Aspose::Words::TabAlignment enum"
linktitle: "TabAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TabAlignment enum. يحدد محاذاة/نوع موضع التبويب في C++."
type: docs
weight: 120000
url: /ar/cpp/aspose.words/tabalignment/
---
## TabAlignment enum


يحدد محاذاة/نوع موضع التبويب.

```cpp
enum class TabAlignment
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| يسار | 0 | يضبط النص إلى اليسار بعد موضع التبويب. |
| وسط | 1 | يُوسّط النص حول موضع التبويب. |
| يمين | 2 | يضبط النص إلى اليمين عند موضع التبويب. |
| Decimal | 3 | يضبط النص عند النقطة العشرية. |
| Bar | 4 | يرسم شريطًا عموديًا في موضع التبويب. |
| List | 6 | التبويب هو فاصل بين الرقم/الرمز النقطي والنص في عنصر القائمة. |
| Clear | 7 | يمسح أي موضع تبويب في هذا الموقع. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
