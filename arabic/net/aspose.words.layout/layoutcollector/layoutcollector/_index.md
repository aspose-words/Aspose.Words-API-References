---
title: LayoutCollector
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ LayoutCollector لتهيئة المثيلات بسلاسة. حسّن كفاءة تطويرك مع هذه الأداة الفعّالة!
type: docs
weight: 10
url: /ar/net/aspose.words.layout/layoutcollector/layoutcollector/
---
## LayoutCollector constructor

يقوم بتهيئة مثيل لهذه الفئة.

```csharp
public LayoutCollector(Document doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | Document | المستند الذي سيتم إرفاق مثيل المجمع به. |

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

* class [Document](../../../aspose.words/document/)
* class [LayoutCollector](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
