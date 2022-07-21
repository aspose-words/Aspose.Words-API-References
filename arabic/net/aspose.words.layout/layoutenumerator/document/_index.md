---
title: Document
second_title: Aspose.Words لمراجع .NET API
description: الحصول على الوثيقة التي تعدادها هذه المثيل .
type: docs
weight: 30
url: /ar/net/aspose.words.layout/layoutenumerator/document/
---
## LayoutEnumerator.Document property

الحصول على الوثيقة التي تعدادها هذه المثيل .

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document)
* class [LayoutEnumerator](../../layoutenumerator)
* مساحة الاسم [Aspose.Words.Layout](../../layoutenumerator)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
