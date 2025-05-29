---
title: LayoutEnumerator.MoveParent
linktitle: MoveParent
articleTitle: MoveParent
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة MoveParent في LayoutEnumerator للتنقل بسهولة إلى الكيانات الأصلية، مما يعزز كفاءة إدارة البيانات لديك.
type: docs
weight: 140
url: /ar/net/aspose.words.layout/layoutenumerator/moveparent/
---
## MoveParent() {#moveparent}

ينتقل إلى الكيان الرئيسي.

```csharp
public bool MoveParent()
```

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

* class [LayoutEnumerator](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)

---

## MoveParent(*[LayoutEntityType](../../layoutentitytype/)*) {#moveparent_1}

ينتقل إلى الكيان الرئيسي للنوع المحدد.

```csharp
public bool MoveParent(LayoutEntityType types)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| types | LayoutEntityType | نوع الكيان الرئيسي المراد الانتقال إليه. استخدم OR بتّيًا لتحديد أنواع رئيسية متعددة. |

## ملاحظات

تكون هذه الطريقة مفيدة إذا كنت بحاجة إلى العثور على الخلية أو العمود أو رأس/تذييل الكيان.

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

* enum [LayoutEntityType](../../layoutentitytype/)
* class [LayoutEnumerator](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
