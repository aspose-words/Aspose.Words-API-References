---
title: "Aspose::Words::Layout::LayoutCollector فئة"
linktitle: "LayoutCollector"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::LayoutCollector فئة. هذه الفئة تسمح بحساب أرقام الصفحات لعقد المستند. لمزيد من المعلومات، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


تسمح هذه الفئة بحساب أرقام الصفحات لعقد المستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutCollector : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clear](./clear/)() | يمسح جميع بيانات التخطيط المجمعة. استدعِ هذه الطريقة بعد تحديث المستند يدويًا، أو إعادة بناء التخطيط. |
| [get_Document](./get_document/)() const | يحصل على أو يضبط المستند الذي تُرفق به هذه المثيل من المجمع. |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على الفهرس القائم على 1 للصفحة التي ينتهي فيها العقدة. يُعيد 0 إذا تعذر ربط العقدة بصفحة. |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يُعيد موضعًا غير شفاف للـ [LayoutEnumerator](../layoutenumerator/) الذي يتطابق مع العقدة المحددة. يمكنك استخدام القيمة المُرجعة كمعامل إلى [Current](../layoutenumerator/get_current/) بشرط أن يكون المستند الجاري تعدادُه هو نفسه مستند العقدة. |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على عدد الصفحات التي تغطيها العقدة المحددة. 0 إذا كانت العقدة ضمن صفحة واحدة. هذا يساوي [GetEndPageIndex()](../) - [GetStartPageIndex()](../). |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على الفهرس القائم على 1 للصفحة التي تبدأ فيها العقدة. يُعيد 0 إذا تعذر ربط العقدة بصفحة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | يُهيئ مثيلًا من هذه الفئة. |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | مُعيّن لـ [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/). |
| static [Type](./type/)() |  |
## ملاحظات


عند إنشاء [LayoutCollector](./) وتحديد كائن [Document](../../aspose.words/document/) لتوصيله، سيقوم المجمع بتسجيل ربط عقد المستند بأجسام التخطيط عندما يتم تنسيق المستند إلى صفحات.

ستتمكن من معرفة على أي صفحة تقع عقدة مستند معينة (مثل run أو paragraph أو خلية جدول) باستخدام طرق [GetStartPageIndex()](../)، [GetEndPageIndex()](../) و[GetNumPagesSpanned()](../). هذه الطرق تبني تلقائيًا نموذج تخطيط الصفحات للمستند وتحدّث الحقول إذا لزم الأمر.

عندما لا تحتاج بعد الآن إلى جمع معلومات التخطيط، من الأفضل ضبط الخاصية [Document](./get_document/) إلى **null** لتجنب جمع غير ضروري لمزيد من ربطات التخطيط.

## أمثلة



يعرض كيفية رؤية نطاقات الصفحات التي تغطيها عقدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// استدعِ طريقة "GetNumPagesSpanned" لحساب عدد الصفحات التي يغطيها محتوى مستندنا.
// نظرًا لأن المستند فارغ، فإن عدد الصفحات الحالي هو صفر.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// املأ المستند بـ 5 صفحات من المحتوى.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// قبل المجمع التخطيطي، نحتاج إلى استدعاء طريقة "UpdatePageLayout" لتزويدنا
// بقيمة دقيقة لأي مقياس متعلق بالتخطيط، مثل عدد الصفحات.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// يمكننا رؤية أرقام الصفحات البداية والنهاية لأي عقدة ومدى الصفحات الإجمالي لها.
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// يمكننا التكرار عبر كيانات التخطيط باستخدام LayoutEnumerator.
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// يمكن لـ LayoutEnumerator عبور مجموعة كيانات التخطيط مثل شجرة.
// يمكننا أيضًا تطبيقه على كيان التخطيط المقابل لأي عقدة.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## انظر أيضًا

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
