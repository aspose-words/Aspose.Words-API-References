---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Layout.LayoutCollector فصل. تسمح هذه الفئة بحساب أرقام الصفحات لعقد المستند في C#.
type: docs
weight: 3320
url: /ar/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

تسمح هذه الفئة بحساب أرقام الصفحات لعقد المستند.

لمعرفة المزيد، قم بزيارة[التحويل إلى تنسيق الصفحة الثابتة](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) مقالة توثيقية.

```csharp
public class LayoutCollector
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [LayoutCollector](layoutcollector/)(*[Document](../../aspose.words/document/)*) | تهيئة مثيل لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | الحصول على أو تعيين المستند الذي تم إرفاق نسخة المجمع به. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | مسح كافة بيانات التخطيط المجمعة. قم باستدعاء هذه الطريقة بعد تحديث المستند يدويًا، أو إعادة إنشاء التخطيط. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | يحصل على فهرس مستند إلى 1 للصفحة التي تنتهي فيها العقدة. يُرجع 0 إذا تعذر تعيين العقدة إلى الصفحة. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | إرجاع موضع معتم للملف[`LayoutEnumerator`](../layoutenumerator/) الذي يتوافق مع العقدة المحددة. يمكنك استخدام القيمة التي تم إرجاعها كوسيطة ل[`Current`](../layoutenumerator/current/) نظرًا لأن الوثيقة التي تم تعدادها ووثيقة العقدة هي نفسها. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | يحصل على عدد الصفحات التي تمتد عليها العقدة المحددة. 0 إذا كانت العقدة ضمن صفحة واحدة. وهذا هو نفسه[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | يحصل على فهرس مستند إلى 1 للصفحة التي تبدأ منها العقدة. يُرجع 0 إذا تعذر تعيين العقدة إلى الصفحة. |

## ملاحظات

عندما تقوم بإنشاء`LayoutCollector` وحدد أ[`Document`](../../aspose.words/document/) كائن المستند الذي سيتم إرفاقه به، سيقوم المجمع بتسجيل تعيين عقد المستند إلى كائنات التخطيط عند تنسيق المستند في صفحات.

ستتمكن من معرفة الصفحة التي توجد بها عقدة مستند معينة (على سبيل المثال التشغيل أو الفقرة أو خلية الجدول) باستخدام[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) و[`GetNumPagesSpanned`](./getnumpagesspanned/)طُرق. تقوم هذه الطرق تلقائيًا بإنشاء نموذج تخطيط الصفحة للمستند وتحديث الحقول إذا لزم الأمر.

عندما لم تعد بحاجة إلى جمع معلومات التخطيط، فمن الأفضل تعيين[`Document`](./document/) الملكية ل`باطل` لتجنب التجميع غير الضروري لمزيد من تعيينات التخطيط.

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

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
