---
title: Class LayoutEnumerator
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Layout.LayoutEnumerator فصل. تعداد كيانات تخطيط الصفحة للمستند. يمكنك استخدام هذه الفئة للتجول في نموذج تخطيط الصفحة. الخصائص المتاحة هي النوع والشكل الهندسي والنص وفهرس الصفحة حيث يتم تقديم الكيان  بالإضافة إلى الهيكل العام والعلاقات . استخدم مزيجًا منGetEntity وCurrent الانتقال إلى الكيان الذي يتوافق مع عقدة المستند.
type: docs
weight: 3140
url: /ar/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

تعداد كيانات تخطيط الصفحة للمستند. يمكنك استخدام هذه الفئة للتجول في نموذج تخطيط الصفحة. الخصائص المتاحة هي النوع والشكل الهندسي والنص وفهرس الصفحة حيث يتم تقديم الكيان ، بالإضافة إلى الهيكل العام والعلاقات . استخدم مزيجًا من[`GetEntity`](../layoutcollector/getentity/) و[`Current`](./current/) الانتقال إلى الكيان الذي يتوافق مع عقدة المستند.

```csharp
public class LayoutEnumerator
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(Document) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | الحصول على أو تعيين الموضع الحالي في نموذج تخطيط الصفحة . هذه الخاصية تُرجع كائنًا معتمًا يتوافق مع كيان التخطيط الحالي. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | الحصول على الوثيقة التي تعدادها هذه المثيل . |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | الحصول على نوع الكيان الحالي. يمكن أن تكون هذه سلسلة فارغة ولكنها ليست فارغة أبدًا. |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | الحصول على الفهرس المستند إلى 1 للصفحة التي تحتوي على الكيان الحالي. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | إرجاع المستطيل المحيط للكيان الحالي بالنسبة إلى الزاوية اليسرى العلوية للصفحة (بالنقاط) . |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | الحصول على نص كيان الامتداد الحالي. رميات لأنواع الكيانات الأخرى. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | يحصل على نوع الكيان الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | ينتقل إلى الكيان الفرعي الأول . |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | ينتقل إلى الكيان الفرعي الأخير . |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | ينتقل إلى الكيان الشقيق التالي بالترتيب المرئي . عند تكرار سطور فقرة مقسمة عبر الصفحات ، لن تنتقل هذه الطريقة إلى الصفحة التالية بل تنتقل إلى الكيان التالي في نفس الصفحة. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | ينتقل إلى الكيان الشقيق التالي بترتيب منطقي . عند تكرار سطور فقرة مقطوعة عبر الصفحات ، ستنتقل هذه الطريقة إلى السطر التالي حتى إذا كانت موجودة في صفحة أخرى. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | ينتقل إلى الكيان الأصلي . |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(LayoutEntityType) | ينتقل إلى الكيان الأصلي من النوع المحدد. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | ينتقل إلى الكيان الشقيق السابق. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | ينتقل إلى الكيان الشقيق السابق بترتيب منطقي . عند تكرار سطور فقرة مقطوعة عبر الصفحات ، ستنتقل هذه الطريقة إلى السطر السابق حتى إذا كانت موجودة في صفحة أخرى. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | نقل العداد إلى الصفحة الأولى من المستند. |

### أمثلة

يعرض طرق اجتياز كيانات تخطيط المستند.

```csharp
public void LayoutEnumerator()
{
    // افتح مستندًا يحتوي على مجموعة متنوعة من كيانات التخطيط.
    // كيانات التخطيط هي الصفحات والخلايا والصفوف والخطوط والكائنات الأخرى المضمنة في تعداد LayoutEntityType.
    // يحتوي كل كيان تخطيط على مساحة مستطيلة يشغلها في نص المستند.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // أنشئ عدادًا يمكنه اجتياز هذه الكيانات مثل الشجرة.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // يمكننا استدعاء هذه الطريقة للتأكد من أن العداد سيكون في كيان التخطيط الأول.
    layoutEnumerator.Reset();

    // هناك أمران يحددان كيفية استمرار عداد التخطيط في اجتياز كيانات التخطيط
    // عندما تواجه كيانات تمتد عبر صفحات متعددة.
    // 1 - بالترتيب المرئي:
    // عند التنقل خلال العناصر الفرعية التابعة لكيان والتي تمتد عبر صفحات متعددة ،
    // يحظى تخطيط الصفحة بالأولوية ، وننتقل إلى العناصر الفرعية الأخرى في هذه الصفحة ونتجنب العناصر الموجودة في التالية.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // العداد الآن في نهاية المجموعة. يمكننا اجتياز كيانات التخطيط للخلف للعودة إلى البداية.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - بالترتيب المنطقي:
    // عند التنقل خلال العناصر الفرعية التابعة لكيان والتي تمتد عبر صفحات متعددة ،
    // سينتقل العداد بين الصفحات لاجتياز جميع الكيانات الفرعية.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// تعداد من خلال تخطيط مجموعة كيانات تخطيط البدل من الأمام إلى الخلف ،
/// بطريقة العمق أولاً وبالترتيب "المرئي".
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
/// تعداد من خلال layoutEnumerator مجموعة كيانات تخطيط back-to-front ،
/// بطريقة العمق أولاً وبالترتيب "المرئي".
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
/// تعداد من خلال تخطيط مجموعة كيانات تخطيط البدل من الأمام إلى الخلف ،
/// بطريقة العمق أولاً وبالترتيب "المنطقي".
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
/// تعداد من خلال layoutEnumerator مجموعة كيانات تخطيط back-to-front ،
/// بطريقة العمق أولاً وبالترتيب "المنطقي".
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
/// طباعة معلومات حول الكيان الحالي لـ layoutEnumerator إلى وحدة التحكم ، أثناء وضع مسافة بادئة للنص بأحرف جدولة
/// استنادًا إلى عمقها بالنسبة إلى عقدة الجذر التي قدمناها في مثيل المُنشئ LayoutEnumerator.
/// يمثل المستطيل الذي نقوم بمعالجته في النهاية المنطقة والموقع اللذين يشغلهما الكيان في المستند.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // فقط الامتدادات يمكن أن تحتوي على نص.
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


