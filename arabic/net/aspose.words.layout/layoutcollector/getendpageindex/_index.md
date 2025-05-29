---
title: LayoutCollector.GetEndPageIndex
linktitle: GetEndPageIndex
articleTitle: GetEndPageIndex
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetEndPageIndex من LayoutCollector للعثور بسهولة على فهرس الصفحة النهائية للعقدة. بسّط عملية ربط صفحاتك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.layout/layoutcollector/getendpageindex/
---
## LayoutCollector.GetEndPageIndex method

يحصل على فهرس الصفحة عند نهاية العقدة بقيمة 1. يُرجع القيمة 0 إذا تعذر ربط العقدة بصفحة.

```csharp
public int GetEndPageIndex(Node node)
```

## أمثلة

يوضح كيفية رؤية نطاقات الصفحات التي تمتد عبرها العقدة.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// قم باستدعاء طريقة "GetNumPagesSpanned" لحساب عدد الصفحات التي يغطيها محتوى مستندنا.
// بما أن المستند فارغ، فإن عدد الصفحات هو صفر حاليًا.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

//إملأ المستند بخمس صفحات من المحتوى.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// قبل جامع التخطيط، نحتاج إلى استدعاء طريقة "UpdatePageLayout" لإعطائنا
// رقم دقيق لأي مقياس مرتبط بالتخطيط، مثل عدد الصفحات.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// يمكننا رؤية أرقام الصفحات الأولية والنهائية لأي عقدة ومدى صفحاتها الإجمالي.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// يمكننا تكرار كيانات التخطيط باستخدام LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// يمكن لـ LayoutEnumerator التنقل عبر مجموعة كيانات التخطيط مثل الشجرة.
//يمكننا أيضًا تطبيقه على أي كيان تخطيط مطابق للعقدة.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### أنظر أيضا

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
