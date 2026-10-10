---
title: "طريقة Aspose::Words::Layout::LayoutCollector::GetEntity"
linktitle: "GetEntity"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Layout::LayoutCollector::GetEntity. تُرجع موضعًا غير شفاف لـ LayoutEnumerator الذي يتطابق مع العقدة المحددة. يمكنك استخدام القيمة المرجعة كمعامل إلى Current بشرط أن يكون المستند الجاري تعدادُه ومستند العقدة هو نفسه في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector::GetEntity method


تُرجع موضعًا غير شفاف لـ [LayoutEnumerator](../../layoutenumerator/) الذي يتطابق مع العقدة المحددة. يمكنك استخدام القيمة المرجعة كمعامل إلى [Current](../../layoutenumerator/get_current/) بشرط أن يكون المستند الجاري تعدادُه ومستند العقدة هو نفسه.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Layout::LayoutCollector::GetEntity(const System::SharedPtr<Aspose::Words::Node> &node)
```

## ملاحظات


تعمل هذه الطريقة فقط مع عقد [Paragraph](../../../aspose.words/paragraph/)، وكذلك العقد الداخلية غير القابلة للتقسيم، مثل [BookmarkStart](../../../aspose.words/bookmarkstart/) أو [Shape](../../../aspose.words.drawing/shape/). لا تعمل مع عقد [Run](../../../aspose.words/run/), [Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) أو [Table](../../../aspose.words.tables/table/)، وكذلك العقد داخل الرأس/التذييل.

لاحظ أن الكيان المرتجع لعقدة [Paragraph](../../../aspose.words/paragraph/) هو فاصل فقرة. استخدم الطريقة المناسبة للصعود إلى السطر الأب.

إذا كنت بحاجة إلى الانتقال إلى [Run](../../../aspose.words/run/) من النص، يمكنك إدراج إشارة مرجعية قبلها ثم الانتقال إلى الإشارة المرجعية بدلاً من ذلك.

إذا كنت بحاجة إلى الانتقال إلى عقدة [Cell](../../../aspose.words.tables/cell/)، يمكنك الانتقال إلى عقدة [Paragraph](../../../aspose.words/paragraph/) داخل هذه الخلية ثم الصعود إلى كيان أب. يمكن استخدام نفس النهج لعقد [Row](../../../aspose.words.tables/row/) و[Table](../../../aspose.words.tables/table/).

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

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
