---
title: CustomXmlProperty.CustomXmlProperty
second_title: Aspose.Words لمراجع .NET API
description: CustomXmlProperty البناء. تهيئة مثيل جديد لهذه الفئة.
type: docs
weight: 10
url: /ar/net/aspose.words.markup/customxmlproperty/customxmlproperty/
---
## CustomXmlProperty constructor

تهيئة مثيل جديد لهذه الفئة.

```csharp
public CustomXmlProperty(string name, string uri, string value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. لا يمكن`باطل`. |
| uri | String | معرف URI لمساحة الاسم الخاص بالخاصية. لا يمكن`باطل`. |
| value | String | قيمة العقار. لا يمكن`باطل`. |

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

* class [CustomXmlProperty](../)
* مساحة الاسم [Aspose.Words.Markup](../../customxmlproperty/)
* المجسم [Aspose.Words](../../../)


