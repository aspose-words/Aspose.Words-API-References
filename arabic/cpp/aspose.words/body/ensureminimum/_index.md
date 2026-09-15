---
title: "Aspose::Words::Body::EnsureMinimum طريقة"
linktitle: "EnsureMinimum"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Body::EnsureMinimum طريقة. إذا لم يكن الطفل الأخير فقرة، ينشئ ويضيف فقرة فارغة واحدة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/body/ensureminimum/
---
## Body::EnsureMinimum method


إذا لم يكن العنصر الفرعي الأخير فقرة، ينشئ ويضيف فقرة فارغة واحدة.

```cpp
void Aspose::Words::Body::EnsureMinimum()
```


## أمثلة



يمسح النص الرئيسي من جميع الأقسام في المستند مع ترك الأقسام نفسها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// يحتوي مستند فارغ على قسم واحد، جسم واحد وفقرة واحدة.
// استدعِ طريقة "RemoveAllChildren" لإزالة جميع تلك العقد،
// وانتهي إلى عقدة مستند بدون أي أبناء.
doc->RemoveAllChildren();

// ليس لهذا المستند الآن أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تعديلها، سنحتاج إلى إعادة ملء مجموعة العقد الخاصة بها.
// أولاً، أنشئ قسمًا جديدًا، ثم أضفه كطفل إلى عقدة المستند الجذرية.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// يحتاج القسم إلى جسم، سيحتوي ويعرض جميع محتوياته
// على الصفحة بين رأس وتذييل القسم.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// هذا الجسم لا يحتوي على عناصر فرعية، لذا لا يمكننا إضافة runs إليه بعد.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// استدعِ "EnsureMinimum" للتأكد من أن هذا الجسم يحتوي على فقرة فارغة واحدة على الأقل.
body->EnsureMinimum();

// الآن، يمكننا إضافة runs إلى الجسم، وجعل المستند يعرضها.
body->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
