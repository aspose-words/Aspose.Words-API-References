---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words لـ .NET
description: LayoutCollector GetEntity طريقة. إرجاع موضع معتم للملفLayoutEnumerator الذي يتوافق مع العقدة المحددة. يمكنك استخدام القيمة التي تم إرجاعها كوسيطة لCurrent نظرًا لأن الوثيقة التي تم تعدادها ووثيقة العقدة هي نفسها في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

إرجاع موضع معتم للملف[`LayoutEnumerator`](../../layoutenumerator/) الذي يتوافق مع العقدة المحددة. يمكنك استخدام القيمة التي تم إرجاعها كوسيطة ل[`Current`](../../layoutenumerator/current/) نظرًا لأن الوثيقة التي تم تعدادها ووثيقة العقدة هي نفسها.

```csharp
public object GetEntity(Node node)
```

## ملاحظات

هذه الطريقة تعمل فقط[`Paragraph`](../../../aspose.words/paragraph/) العقد، وكذلك العقد المضمنة غير القابلة للتجزئة، على سبيل المثال[`BookmarkStart`](../../../aspose.words/bookmarkstart/) أو[`Shape`](../../../aspose.words.drawing/shape/) . لا يعمل من أجل[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) أو[`Table`](../../../aspose.words.tables/table/) العقد والعقد داخل الرأس/التذييل.

لاحظ أن الكيان عاد لـ a[`Paragraph`](../../../aspose.words/paragraph/) العقدة عبارة عن فترة فاصل للفقرة. استخدم الطريقة المناسبة للصعود إلى السطر الأصلي

إذا كنت بحاجة إلى الانتقال إلى أ[`Run`](../../../aspose.words/run/) من النص، فيمكنك إدراج إشارة مرجعية قبل it مباشرة ثم الانتقال إلى الإشارة المرجعية بدلاً من ذلك.

إذا كنت بحاجة إلى الانتقال إلى أ[`Cell`](../../../aspose.words.tables/cell/) عقدة ثم يمكنك الانتقال إلى[`Paragraph`](../../../aspose.words/paragraph/)عقدة في هذه الخلية ثم اصعد إلى الكيان الأصلي. يمكن استخدام نفس النهج ل[`Row`](../../../aspose.words.tables/row/) و[`Table`](../../../aspose.words.tables/table/) العقد.

## أمثلة

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
