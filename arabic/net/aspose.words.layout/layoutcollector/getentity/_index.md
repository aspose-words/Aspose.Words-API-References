---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة LayoutCollector GetEntity، واسترد موضع LayoutEnumerator بسهولة للتنقل السلس في المستندات وتحسين الإنتاجية.
type: docs
weight: 50
url: /ar/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

يعيد موضعًا معتمًا لـ[`LayoutEnumerator`](../../layoutenumerator/) الذي يتوافق مع العقدة المحددة. يمكنك استخدام القيمة المرتجعة كحجة لـ[`Current`](../../layoutenumerator/current/) نظرًا لأن المستند الذي يتم تعداده هو ومستند العقدة هما نفس الشيء.

```csharp
public object GetEntity(Node node)
```

## ملاحظات

هذه الطريقة تعمل فقط مع[`Paragraph`](../../../aspose.words/paragraph/) العقد، وكذلك العقد المضمنة غير القابلة للتجزئة، على سبيل المثال[`BookmarkStart`](../../../aspose.words/bookmarkstart/) أو[`Shape`](../../../aspose.words.drawing/shape/) .إنه لا يعمل ل[`Run`](../../../aspose.words/run/) ،[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) أو[`Table`](../../../aspose.words.tables/table/) العقد، والعقد داخل الرأس/التذييل.

لاحظ أن الكيان تم إرجاعه لـ[`Paragraph`](../../../aspose.words/paragraph/)العقدة هي امتداد لفاصل الفقرة. استخدم الطريقة المناسبة للصعود إلى السطر الرئيسي.

إذا كنت بحاجة إلى التنقل إلى[`Run`](../../../aspose.words/run/) من النص، يمكنك إدراج إشارة مرجعية مباشرة قبل it ثم الانتقال إلى الإشارة المرجعية بدلاً من ذلك.

إذا كنت بحاجة إلى التنقل إلى[`Cell`](../../../aspose.words.tables/cell/) العقدة ثم يمكنك الانتقال إلى[`Paragraph`](../../../aspose.words/paragraph/) عقدة في هذه الخلية، ثم تصعد إلى الكيان الرئيسي. يمكن استخدام نفس الطريقة لـ[`Row`](../../../aspose.words.tables/row/) و[`Table`](../../../aspose.words.tables/table/) العقد.

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
