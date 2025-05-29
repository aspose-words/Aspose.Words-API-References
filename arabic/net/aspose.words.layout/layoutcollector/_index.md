---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Layout.LayoutCollector لحساب أرقام صفحات عقدة المستند بكفاءة، مما يعزز تجربة إدارة المستندات لديك.
type: docs
weight: 3770
url: /ar/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

تسمح هذه الفئة بحساب أرقام الصفحات الخاصة بعقد المستندات.

لمعرفة المزيد، قم بزيارة[التحويل إلى تنسيق الصفحة الثابتة](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) مقالة توثيقية.

```csharp
public class LayoutCollector
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [LayoutCollector](layoutcollector/)(*[Document](../../aspose.words/document/)*) | يقوم بتهيئة مثيل لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | يحصل على المستند الذي تم إرفاق مثيل المجمع به أو يعينه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | يمسح جميع بيانات التخطيط المجمعة. استدعي هذه الطريقة بعد تحديث المستند يدويًا، أو إعادة بناء التخطيط. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | يحصل على فهرس الصفحة عند نهاية العقدة بقيمة 1. يُرجع القيمة 0 إذا تعذر ربط العقدة بصفحة. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | يعيد موضعًا معتمًا لـ[`LayoutEnumerator`](../layoutenumerator/) الذي يتوافق مع العقدة المحددة. يمكنك استخدام القيمة المرتجعة كحجة لـ[`Current`](../layoutenumerator/current/) نظرًا لأن المستند الذي يتم تعداده هو ومستند العقدة هما نفس الشيء. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | يحصل على عدد الصفحات التي تمتد إليها العقدة المحددة. 0 إذا كانت العقدة ضمن صفحة واحدة. هذا هو نفس[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | يحصل على فهرس الصفحة التي تبدأ منها العقدة بقيمة 1. يُرجع القيمة 0 إذا تعذر ربط العقدة بصفحة. |

## ملاحظات

عندما تقوم بإنشاء`LayoutCollector` وحدد[`Document`](../../aspose.words/document/)كائن المستند المراد إرفاقه به، سوف يسجل المجمع تعيين عقد المستند إلى كائنات التخطيط عندما يتم تنسيق المستند إلى صفحات.

ستتمكن من معرفة الصفحة التي توجد بها عقدة مستند معينة (مثل تشغيل أو فقرة أو خلية جدول) باستخدام[`GetStartPageIndex`](./getstartpageindex/) ،[`GetEndPageIndex`](./getendpageindex/) و[`GetNumPagesSpanned`](./getnumpagesspanned/) الأساليب. تقوم هذه الأساليب تلقائيًا ببناء نموذج تخطيط الصفحة للمستند وتحديث الحقول إذا لزم الأمر.

عندما لم تعد بحاجة إلى جمع معلومات التخطيط، فمن الأفضل ضبط[`Document`](./document/) الممتلكات إلى`باطل` لتجنب التجميع غير الضروري لمزيد من تعيينات التخطيط.

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

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
