---
title: Class SmartTag
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.SmartTag فصل. يحدد هذا العنصر وجود علامة ذكية حول واحد أو أكثر من الهياكل المضمنة عمليات التشغيل  الصور  الحقول  إلخ داخل فقرة.
type: docs
weight: 3810
url: /ar/net/aspose.words.markup/smarttag/
---
## SmartTag class

يحدد هذا العنصر وجود علامة ذكية حول واحد أو أكثر من الهياكل المضمنة (عمليات التشغيل ، الصور ، الحقول ، إلخ) داخل فقرة.

```csharp
public class SmartTag : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [SmartTag](smarttag/)(DocumentBase) | يقوم بتهيئة مثيل جديد لملف`SmartTag` فئة . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count/) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص . |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [Element](../../aspose.words.markup/smarttag/element/) { get; set; } | يحدد اسم العلامة الذكية داخل المستند. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | الحصول على الطفل الأول للعقدة . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | الحصول على آخر تابع للعقدة . |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.markup/smarttag/nodetype/) { get; } | عوائد **NodeType.SmartTag** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Properties](../../aspose.words.markup/smarttag/properties/) { get; } | مجموعة من خصائص العلامات الذكية . |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [Uri](../../aspose.words.markup/smarttag/uri/) { get; set; } | يحدد مساحة الاسم URI للعلامة الذكية. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.markup/smarttag/accept/)(DocumentVisitor) | يقبل الزائر . |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [Clone](../../aspose.words/node/clone/)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة . |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة . |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل كافة العقد التابعة للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل`SmartTag` العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

العلامات الذكية هي نوع من ترميز XML المخصص. توفر العلامات الذكية وسيلة لتضمين الدلالات المعرفة من قبل العميل في المستند من خلال القدرة على توفير مساحة اسم أساسية / name لتشغيل أو مجموعة من عمليات التشغيل داخل المستند.

`SmartTag` يمكن أن يكون طفلًا من[`Paragraph`](../../aspose.words/paragraph/) or آخر`SmartTag` العقدة.

تتكون القائمة الكاملة للعقد الفرعية التي يمكن أن تحدث داخل العلامة الذكية من [`BookmarkStart`](../../aspose.words/bookmarkstart/) و[`BookmarkEnd`](../../aspose.words/bookmarkend/) ، [`FieldStart`](../../aspose.words.fields/fieldstart/) و[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) و[`FieldEnd`](../../aspose.words.fields/fieldend/) و[`FormField`](../../aspose.words.fields/formfield/) ، [`Comment`](../../aspose.words/comment/) و[`Footnote`](../../aspose.words.notes/footnote/) ، [`Run`](../../aspose.words/run/) و[`SpecialChar`](../../aspose.words/specialchar/) ، [`Shape`](../../aspose.words.drawing/shape/) و[`GroupShape`](../../aspose.words.drawing/groupshape/) ، [`CommentRangeStart`](../../aspose.words/commentrangestart/) ، [`CommentRangeEnd`](../../aspose.words/commentrangeend/) ، `SmartTag`.

### أمثلة

يوضح كيفية إنشاء العلامات الذكية.

```csharp
public void Create()
{
    Document doc = new Document();

    // تظهر علامة ذكية في مستند مع Microsoft Word يتعرف على جزء من نصه كشكل من أشكال البيانات ،
    // مثل الاسم أو التاريخ أو العنوان ، ويحوله إلى ارتباط تشعبي يعرض تسطيرًا منقطًا بنفسجي اللون.
    SmartTag smartTag = new SmartTag(doc);

    // العلامات الذكية عبارة عن عقد مركبة تحتوي على نص تم التعرف عليه بالكامل.
    // أضف محتويات إلى هذه العلامة الذكية يدويًا.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // قد يتعرف Microsoft Word على المحتويات المذكورة أعلاه على أنها تاريخ.
    // تستخدم العلامات الذكية خاصية "العنصر" لتعكس نوع البيانات التي تحتوي عليها.
    smartTag.Element = "date";

    // تقوم بعض أنواع العلامات الذكية بمعالجة محتوياتها بشكل أكبر في خصائص XML المخصصة.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // اضبط عنوان URI للعلامة الذكية على القيمة الافتراضية.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // إنشاء علامة ذكية أخرى لمؤشر الأسهم.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // طباعة جميع العلامات الذكية في وثيقتنا باستخدام زائر المستند.
    doc.Accept(new SmartTagPrinter());

    // تدعم الإصدارات القديمة من Microsoft Word العلامات الذكية.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // استخدم طريقة "RemoveSmartTags" لإزالة كافة العلامات الذكية من المستند.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// تمت زيارة المطبوعات للعلامات الذكية ومحتوياتها.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة SmartTag في المستند.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند انتهاء زيارة عقدة SmartTag.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### أنظر أيضا

* class [CompositeNode](../../aspose.words/compositenode/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


