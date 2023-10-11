---
title: SmartTag.SmartTag
second_title: Aspose.Words لمراجع .NET API
description: SmartTag البناء. تهيئة مثيل جديد لـSmartTag فئة.
type: docs
weight: 10
url: /ar/net/aspose.words.markup/smarttag/smarttag/
---
## SmartTag constructor

تهيئة مثيل جديد لـ[`SmartTag`](../) فئة.

```csharp
public SmartTag(DocumentBase doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |

### ملاحظات

عندما تقوم بإنشاء عقدة جديدة، يجب عليك تحديد المستند الذي تنتمي إليه العقدة. لا يمكن أن توجد العقدة بدون مستند لأنها تعتمد على الهياكل على مستوى المستند مثل القوائم والأنماط. على الرغم من أن العقدة تنتمي دائمًا إلى مستند، إلا أن العقدة قد تكون أو لا تكون جزءًا من شجرة المستندات.

عند إنشاء عقدة، فإنها تنتمي إلى مستند، ولكنها ليست بعد جزءًا من شجرة المستند و[`ParentNode`](../../../aspose.words/node/parentnode/) يكون`باطل` . لإدراج عقدة في المستند، استخدم Node) أوNode) methods على العقدة الأصلية.

### أمثلة

يوضح كيفية إنشاء العلامات الذكية.

```csharp
public void Create()
{
    Document doc = new Document();

    // العلامة الذكية التي تظهر في مستند باستخدام Microsoft Word تتعرف على جزء من نصه كشكل من أشكال البيانات،
    // مثل الاسم أو التاريخ أو العنوان، وتحويله إلى ارتباط تشعبي يعرض تسطيرًا منقطًا أرجوانيًا.
    SmartTag smartTag = new SmartTag(doc);

    // العلامات الذكية هي عقد مركبة تحتوي على النص الذي تم التعرف عليه بالكامل.
    // أضف محتويات إلى هذه العلامة الذكية يدويًا.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // قد يتعرف Microsoft Word على المحتويات المذكورة أعلاه على أنها تاريخ.
    // تستخدم العلامات الذكية خاصية "العنصر" لتعكس نوع البيانات التي تحتوي عليها.
    smartTag.Element = "date";

    // تقوم بعض أنواع العلامات الذكية بمعالجة محتوياتها بشكل أكبر في خصائص XML المخصصة.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // قم بتعيين URI الخاص بالعلامة الذكية على القيمة الافتراضية.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // أنشئ علامة ذكية أخرى لمؤشر الأسهم.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // اطبع جميع العلامات الذكية في مستندنا باستخدام زائر المستند.
    doc.Accept(new SmartTagPrinter());

    // الإصدارات الأقدم من Microsoft Word تدعم العلامات الذكية.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // استخدم طريقة "RemoveSmartTags" لإزالة كافة العلامات الذكية من المستند.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// طباعة العلامات الذكية التي تمت زيارتها ومحتوياتها.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة SmartTag في المستند.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند انتهاء زيارة عقدة SmartTag.
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [SmartTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../smarttag/)
* المجسم [Aspose.Words](../../../)


