---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Layout.LayoutEnumerator فصل. تعداد كيانات تخطيط الصفحة الخاصة بالمستند. يمكنك استخدام هذه الفئة للتجول في نموذج تخطيط الصفحة. الخصائص المتاحة هي النوع والهندسة والنص وفهرس الصفحة حيث يتم عرض الكيان بالإضافة إلى البنية والعلاقات العامة. استخدم مجموعة منGetEntity وCurrent انتقل إلى الكيان الذي يتوافق مع عقدة المستند في C#.
type: docs
weight: 3340
url: /ar/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

تعداد كيانات تخطيط الصفحة الخاصة بالمستند. يمكنك استخدام هذه الفئة للتجول في نموذج تخطيط الصفحة. الخصائص المتاحة هي النوع والهندسة والنص وفهرس الصفحة حيث يتم عرض الكيان، بالإضافة إلى البنية والعلاقات العامة. استخدم مجموعة من[`GetEntity`](../layoutcollector/getentity/) و[`Current`](./current/) انتقل إلى الكيان الذي يتوافق مع عقدة المستند.

لمعرفة المزيد، قم بزيارة[التحويل إلى تنسيق الصفحة الثابتة](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) مقالة توثيقية.

```csharp
public class LayoutEnumerator
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(*[Document](../../aspose.words/document/)*) | تهيئة المثيل الجديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | الحصول على الموضع الحالي في نموذج تخطيط الصفحة أو تعيينه. تقوم هذه الخاصية بإرجاع كائن معتم يتوافق مع كيان التخطيط الحالي. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | الحصول على المستند الذي تم تعداده في هذا المثيل. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | الحصول على خاصية مسماة للكيان. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | الحصول على نوع الكيان الحالي. يمكن أن تكون هذه سلسلة فارغة ولكن أبدًا`باطل` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | الحصول على الفهرس المستند إلى 1 للصفحة التي تحتوي على الكيان الحالي. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | إرجاع المستطيل المحيط للكيان الحالي بالنسبة إلى الزاوية اليسرى العليا للصفحة (بالنقاط). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | يحصل على نص كيان الامتداد الحالي. رميات لأنواع الكيانات الأخرى. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | الحصول على نوع الكيان الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | للانتقال إلى الكيان الفرعي الأول. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | للانتقال إلى الكيان الفرعي الأخير. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | ينتقل إلى الكيان الشقيق التالي بالترتيب المرئي. عند تكرار أسطر فقرة متقطعة عبر الصفحات، لن تنتقل هذه الطريقة إلى الصفحة التالية بل ستنتقل إلى الكيان التالي في نفس الصفحة. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | ينتقل إلى الكيان الشقيق التالي بترتيب منطقي. عند تكرار أسطر فقرة متقطعة عبر الصفحات، ستنتقل هذه الطريقة إلى السطر التالي حتى لو كان موجودًا في صفحة أخرى. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | ينتقل إلى الكيان الأصلي. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | للانتقال إلى الكيان الأصلي للنوع المحدد. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | ينتقل إلى الكيان الشقيق السابق. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | ينتقل إلى الكيان الشقيق السابق بترتيب منطقي. عند تكرار أسطر فقرة متقطعة عبر الصفحات، ستنتقل هذه الطريقة إلى السطر السابق حتى لو كان موجودًا في صفحة أخرى. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | ينقل العداد إلى الصفحة الأولى من المستند. |

## أمثلة

يُظهر طرق اجتياز كيانات تخطيط المستند.

```csharp
public void LayoutEnumerator()
{
    // افتح مستندًا يحتوي على مجموعة متنوعة من كيانات التخطيط.
    // كيانات التخطيط هي الصفحات والخلايا والصفوف والخطوط والكائنات الأخرى المضمنة في LayoutEntityType enum.
    // يحتوي كل كيان تخطيط على مساحة مستطيلة يشغلها في نص المستند.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // قم بإنشاء عداد يمكنه اجتياز هذه الكيانات مثل الشجرة.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // يمكننا استدعاء هذه الطريقة للتأكد من أن العداد سيكون في كيان التخطيط الأول.
    layoutEnumerator.Reset();

    // هناك أمران يحددان كيفية استمرار عداد التخطيط في اجتياز كيانات التخطيط
    // عندما يواجه كيانات تمتد عبر صفحات متعددة.
    // 1 - بالترتيب المرئي:
    // عند التنقل بين العناصر التابعة للكيان والتي تمتد على عدة صفحات،
    // تخطيط الصفحة له الأولوية، وننتقل إلى العناصر الفرعية الأخرى في هذه الصفحة ونتجنب العناصر الموجودة في الصفحة التالية.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // أصبح العداد لدينا الآن في نهاية المجموعة. يمكننا اجتياز كيانات التخطيط للخلف للعودة إلى البداية.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - بالترتيب المنطقي:
    // عند التنقل بين العناصر التابعة للكيان والتي تمتد على عدة صفحات،
    // سيتنقل العداد بين الصفحات لاجتياز جميع الكيانات الفرعية.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// التعداد من خلال مجموعة كيانات تخطيط LayoutEnumerator من الأمام إلى الخلف،
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
/// التعداد من خلال مجموعة كيانات تخطيط LayoutEnumerator من الخلف إلى الأمام،
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
/// التعداد من خلال مجموعة كيانات تخطيط LayoutEnumerator من الأمام إلى الخلف،
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
/// التعداد من خلال مجموعة كيانات تخطيط LayoutEnumerator من الخلف إلى الأمام،
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
/// اطبع معلومات حول الكيان الحالي لـ LayoutEnumerator إلى وحدة التحكم، مع وضع مسافة بادئة للنص باستخدام أحرف الجدولة
/// استنادًا إلى عمقها بالنسبة إلى العقدة الجذرية التي قدمناها في مثيل LayoutEnumerator المُنشئ.
/// يمثل المستطيل الذي نقوم بمعالجته في النهاية المنطقة والموقع الذي يشغله الكيان في المستند.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // الامتدادات فقط هي التي يمكن أن تحتوي على نص.
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
