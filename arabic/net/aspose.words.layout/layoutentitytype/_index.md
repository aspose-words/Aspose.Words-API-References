---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Layout.LayoutEntityType enum، الذي يتميز بأنواع مختلفة من كيانات التخطيط لتحسين تنسيق المستندات والتكامل السلس.
type: docs
weight: 3780
url: /ar/net/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enumeration

أنواع كيانات التخطيط.

```csharp
[Flags]
public enum LayoutEntityType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | القيمة الافتراضية. |
| Page | `1` | يمثل صفحة من المستند. قد تحتوي الصفحة علىColumn ،HeaderFooter وComment الكيانات الفرعية. |
| Column | `2` | يمثل عمودًا من النص على الصفحة. قد يحتوي العمود على نفس الكيانات الفرعية مثلCell ، بالإضافة إلىFootnote ،Endnote وNoteSeparator الكيانات. |
| Row | `8` | يمثل صف جدول. قد يحتوي الصف علىCell ككيانات فرعية. |
| Cell | `10` | يمثل خلية جدول. قد تحتوي الخلية علىLine وRow الكيانات الفرعية. |
| Line | `20` | يمثل سطرًا من أحرف النص والكائنات المضمنة. قد يحتوي السطر علىSpan الكيانات الفرعية. |
| Span | `40` | يمثل حرفًا واحدًا أو أكثر في سطر. يتضمن ذلك أحرفًا خاصة مثل علامات بداية/نهاية الحقل والإشارات المرجعية والتعليقات. قد لا يحتوي Span على كيانات فرعية. |
| Footnote | `100` | يمثل عنصر نائب لمحتوى الحاشية السفلية. قد تحتوي الحاشية السفلية علىNote الكيانات الفرعية. |
| Endnote | `200` | يمثل عنصر نائب لمحتوى الحاشية الختامية. قد تحتوي الحاشية الختامية علىNote الكيانات الفرعية. |
| Note | `4000` | يمثل عنصر نائب لمحتوى الملاحظة. قد تحتوي الملاحظة علىLine وRow الكيانات الفرعية. |
| HeaderFooter | `400` | يمثل عنصر نائب لمحتوى الرأس/التذييل على الصفحة. قد يحتوي HeaderFooter علىLine وRow الكيانات الفرعية. |
| TextBox | `800` | يمثل منطقة النص داخل الشكل. قد يحتوي مربع النص علىLine وRow الكيانات الفرعية. |
| Comment | `1000` | يمثل عنصر نائب لمحتوى التعليق. قد يحتوي التعليق علىLine وRow الكيانات الفرعية. |
| NoteSeparator | `2000` | يمثل فاصل الحاشية السفلية/الحاشية النهائية. قد يحتوي فاصل الملاحظات علىLine وRow الكيانات الفرعية. |

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
