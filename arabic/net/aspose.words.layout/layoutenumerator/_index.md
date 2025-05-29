---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Layout.LayoutEnumerator لتعداد تخطيطات المستندات بكفاءة. استكشف هندسة الصفحات والنصوص والبنية بكل سهولة!
type: docs
weight: 3790
url: /ar/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

يُحصي كيانات تخطيط الصفحة في مستند. يمكنك استخدام هذه الفئة لاستعراض نموذج تخطيط الصفحة. الخصائص المتاحة هي النوع، والهندسة، والنص، وفهرس الصفحة حيث يتم عرض الكيان، بالإضافة إلى البنية العامة والعلاقات. استخدم مزيجًا من[`GetEntity`](../layoutcollector/getentity/) و[`Current`](./current/) انتقل إلى الكيان الذي يتوافق مع عقدة المستند.

لمعرفة المزيد، قم بزيارة[التحويل إلى تنسيق الصفحة الثابتة](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) مقالة توثيقية.

```csharp
public class LayoutEnumerator
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(*[Document](../../aspose.words/document/)*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | يحصل على الموضع الحالي في نموذج تخطيط الصفحة أو يعينه. تعيد هذه الخاصية كائنًا غير شفاف يتوافق مع كيان التخطيط الحالي. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | يحصل على المستند الذي تعده هذه المثيلات. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | يحصل على خاصية مسماة للكيان. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | يحصل على نوع الكيان الحالي. يمكن أن يكون سلسلة فارغة، ولكن لا`باطل` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | يحصل على الفهرس القائم على 1 للصفحة التي تحتوي على الكيان الحالي. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | يعيد المستطيل المحيط بالكيان الحالي بالنسبة إلى الزاوية العلوية اليسرى للصفحة (بالنقاط). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | يسترجع نص كيان النطاق الحالي. يُرمى لأنواع الكيانات الأخرى. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | يحصل على نوع الكيان الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | ينتقل إلى الكيان الفرعي الأول. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | ينتقل إلى الكيان الفرعي الأخير. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | ينتقل إلى الكيان الشقيق التالي بالترتيب المرئي. عند تكرار أسطر فقرة مقسمة عبر الصفحات، لن تنتقل هذه الطريقة إلى الصفحة التالية، بل ستنتقل إلى الكيان التالي على نفس الصفحة. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | ينتقل إلى الكيان الشقيق التالي بترتيب منطقي. عند تكرار أسطر فقرة مقسمة عبر الصفحات، ستنتقل هذه الطريقة إلى السطر التالي حتى لو كان موجودًا في صفحة أخرى. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | ينتقل إلى الكيان الرئيسي. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | ينتقل إلى الكيان الرئيسي للنوع المحدد. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | ينتقل إلى الكيان الشقيق السابق. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | ينتقل إلى الكيان الشقيق السابق بترتيب منطقي. عند تكرار أسطر فقرة مقسمة عبر الصفحات، ستنتقل هذه الطريقة إلى السطر السابق حتى لو كان موجودًا في صفحة أخرى. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | ينقل المُعدِّد إلى الصفحة الأولى من المستند. |

## أمثلة

يُظهر طرقًا لاجتياز كيانات تخطيط المستند.

```csharp
public void LayoutEnumerator()
{
    // افتح مستندًا يحتوي على مجموعة متنوعة من كيانات التخطيط.
    // كيانات التخطيط هي الصفحات والخلايا والصفوف والأسطر والكائنات الأخرى المضمنة في LayoutEntityType.
    // يحتوي كل كيان تخطيط على مساحة مستطيلة يشغلها في نص المستند.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // قم بإنشاء مُعَدِّد يمكنه عبور هذه الكيانات مثل الشجرة.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // يمكننا استدعاء هذه الطريقة للتأكد من أن المُعدِّد سيكون في كيان التخطيط الأول.
    layoutEnumerator.Reset();

    // هناك أمران يحددان كيفية استمرار مُعَدِّد التخطيط في عبور كيانات التخطيط
    // عندما يواجه كيانات تمتد عبر صفحات متعددة.
    // 1 - بالترتيب المرئي:
    // عند التنقل عبر أبناء الكيان الذين يمتدون عبر صفحات متعددة،
    // تخطيط الصفحة له الأولوية، ونحن ننتقل إلى عناصر فرعية أخرى في هذه الصفحة ونتجنب العناصر الموجودة في الصفحة التالية.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // أصبح مُعَدِّدنا الآن في نهاية المجموعة. يُمكننا اجتياز عناصر التخطيط للخلف للعودة إلى البداية.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - بالترتيب المنطقي:
    // عند التنقل عبر أبناء الكيان الذين يمتدون عبر صفحات متعددة،
    // سوف ينتقل المُعدِّد بين الصفحات لاجتياز جميع الكيانات الفرعية.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// قم بالترقيم من خلال مجموعة كيان تخطيط layoutEnumerator من الأمام إلى الخلف،
/// بطريقة العمق أولاً، وبالترتيب "المرئي".
/// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNext());
}

/// <summary>
/// قم بالترقيم من خلال مجموعة كيان تخطيط layoutEnumerator من الخلف إلى الأمام،
/// بطريقة العمق أولاً، وبالترتيب "المرئي".
/// </summary>
private static void TraverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePrevious());
}

/// <summary>
/// قم بالترقيم من خلال مجموعة كيان تخطيط layoutEnumerator من الأمام إلى الخلف،
/// بطريقة العمق أولاً، وبالترتيب "المنطقي".
/// </summary>
private static void TraverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNextLogical());
}

/// <summary>
/// قم بالترقيم من خلال مجموعة كيان تخطيط layoutEnumerator من الخلف إلى الأمام،
/// بطريقة العمق أولاً، وبالترتيب "المنطقي".
/// </summary>
private static void TraverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePreviousLogical());
}

/// <summary>
/// اطبع معلومات حول كيان layoutEnumerator الحالي في وحدة التحكم، مع وضع مسافة بادئة للنص باستخدام أحرف الجدولة
/// بناءً على عمقها النسبي لعقدة الجذر التي قدمناها في مثيل المنشئ LayoutEnumerator.
/// المستطيل الذي نقوم بمعالجته في النهاية يمثل المساحة والموقع الذي تشغله الكيان في المستند.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // فقط النطاقات يمكن أن تحتوي على نص.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
