---
title: LayoutCollector.Clear
second_title: Aspose.Words لمراجع .NET API
description: LayoutCollector طريقة. مسح كافة بيانات التخطيط المجمعة. قم باستدعاء هذه الطريقة بعد تحديث المستند يدويًا أو إعادة إنشاء التخطيط.
type: docs
weight: 30
url: /ar/net/aspose.words.layout/layoutcollector/clear/
---
## LayoutCollector.Clear method

مسح كافة بيانات التخطيط المجمعة. قم باستدعاء هذه الطريقة بعد تحديث المستند يدويًا، أو إعادة إنشاء التخطيط.

```csharp
public void Clear()
```

### أمثلة

يوضح كيفية رؤية نطاقات الصفحات التي تمتد عليها العقدة.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// اتصل بطريقة "GetNumPagesSpanned" لحساب عدد الصفحات التي يغطيها محتوى وثيقتنا.
// بما أن المستند فارغ، فإن عدد الصفحات هذا هو صفر حاليًا.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// املأ المستند بخمس صفحات من المحتوى.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// قبل تجميع التخطيط، نحتاج إلى استدعاء طريقة "UpdatePageLayout" لتعطينا
// رقم دقيق لأي مقياس متعلق بالتخطيط، مثل عدد الصفحات.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// يمكننا رؤية أرقام صفحات البداية والنهاية لأي عقدة وامتداد صفحاتها الإجمالي.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// يمكننا التكرار على كيانات التخطيط باستخدام LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// يمكن لـ LayoutEnumerator اجتياز مجموعة كيانات التخطيط مثل الشجرة.
// يمكننا أيضًا تطبيقه على كيان التخطيط المقابل لأي عقدة.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### أنظر أيضا

* class [LayoutCollector](../)
* مساحة الاسم [Aspose.Words.Layout](../../layoutcollector/)
* المجسم [Aspose.Words](../../../)


