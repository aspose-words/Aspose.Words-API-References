---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Layout.LayoutEntityType تعداد. أنواع كيانات التخطيط في C#.
type: docs
weight: 3330
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
| Page | `1` | يمثل صفحة من المستند. قد تحتوي الصفحة علىColumn ,HeaderFooter وComment الكيانات الفرعية. |
| Column | `2` | يمثل عمود نص في الصفحة. قد يحتوي العمود على نفس الكيانات الفرعية مثلCell بالإضافة إلىFootnote ,Endnote وNoteSeparator الكيانات. |
| Row | `8` | يمثل صف جدول. قد يحتوي الصف علىCell ككيانات فرعية. |
| Cell | `10` | تمثل خلية جدول. قد تحتوي الخلية علىLine وRow الكيانات الفرعية. |
| Line | `20` | يمثل سطرًا من أحرف النص والكائنات المضمنة. قد يحتوي السطر علىSpan الكيانات الفرعية. |
| Span | `40` | يمثل حرفًا واحدًا أو أكثر في السطر. يتضمن ذلك أحرفًا خاصة مثل علامات بداية/نهاية الحقل والإشارات المرجعية والتعليقات. قد لا يحتوي Span على كيانات فرعية. |
| Footnote | `100` | يمثل العنصر النائب لمحتوى الحواشي السفلية. قد تحتوي الحاشية السفلية علىNote الكيانات الفرعية. |
| Endnote | `200` | يمثل العنصر النائب لمحتوى التعليق الختامي. قد يكون للتعليق الختاميNote الكيانات الفرعية. |
| Note | `4000` | يمثل العنصر النائب لمحتوى الملاحظة. قد تحتوي الملاحظة علىLine وRow الكيانات الفرعية. |
| HeaderFooter | `400` | يمثل العنصر النائب لمحتوى الرأس/التذييل على الصفحة. قد يحتوي رأس التذييل علىLine وRow الكيانات الفرعية. |
| TextBox | `800` | يمثل منطقة النص داخل الشكل. قد يحتوي مربع النص علىLine وRow الكيانات الفرعية. |
| Comment | `1000` | يمثل العنصر النائب لمحتوى التعليق. قد يحتوي التعليق علىLine وRow الكيانات الفرعية. |
| NoteSeparator | `2000` | يمثل فاصل الحواشي السفلية/التعليقات الختامية. قد يحتوي فاصل الملاحظات علىLine وRow الكيانات الفرعية. |

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
