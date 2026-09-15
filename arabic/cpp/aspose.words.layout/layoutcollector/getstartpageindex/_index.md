---
title: "طريقة Aspose::Words::Layout::LayoutCollector::GetStartPageIndex"
linktitle: "GetStartPageIndex"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Layout::LayoutCollector::GetStartPageIndex. يحصل على الفهرس القائم على 1 للصفحة التي يبدأ فيها العقدة. يرجع 0 إذا تعذر ربط العقدة بصفحة في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.layout/layoutcollector/getstartpageindex/
---
## LayoutCollector::GetStartPageIndex method


يحصل على الفهرس القائم على 1 للصفحة التي تبدأ فيها العقدة. يُعيد 0 إذا تعذر ربط العقدة بصفحة.

```cpp
int32_t Aspose::Words::Layout::LayoutCollector::GetStartPageIndex(const System::SharedPtr<Aspose::Words::Node> &node)
```


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
