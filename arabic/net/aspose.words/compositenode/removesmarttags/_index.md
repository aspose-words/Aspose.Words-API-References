---
title: CompositeNode.RemoveSmartTags
linktitle: RemoveSmartTags
articleTitle: RemoveSmartTags
second_title: Aspose.Words لـ .NET
description: قم بتنظيف CompositeNode الخاص بك بسهولة باستخدام طريقة RemoveSmartTags، مما يؤدي إلى إزالة جميع أحفاد SmartTag لإدارة البيانات بشكل مبسط.
type: docs
weight: 200
url: /ar/net/aspose.words/compositenode/removesmarttags/
---
## CompositeNode.RemoveSmartTags method

يزيل الكل[`SmartTag`](../../../aspose.words.markup/smarttag/) العقد المنحدرة من العقدة الحالية.

```csharp
public void RemoveSmartTags()
```

## ملاحظات

لا تؤدي هذه الطريقة إلى إزالة محتوى العلامات الذكية.

## أمثلة

يقوم بإزالة جميع العلامات الذكية من العقد التابعة للعقدة المركبة.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

Assert.AreEqual(8, doc.GetChildNodes(NodeType.SmartTag, true).Count);

doc.RemoveSmartTags();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
```

يوضح كيفية إنشاء العلامات الذكية.

```csharp
public void Create()
{
    Document doc = new Document();

    // تظهر علامة ذكية في مستند باستخدام Microsoft Word تتعرف على جزء من نصه كنوع من البيانات،
    // مثل الاسم أو التاريخ أو العنوان، وتحويله إلى ارتباط تشعبي يعرض خطًا منقطًا باللون الأرجواني.
    SmartTag smartTag = new SmartTag(doc);

    // العلامات الذكية عبارة عن عقد مركبة تحتوي على النص المعترف به بالكامل.
    //أضف المحتويات إلى هذه العلامة الذكية يدويًا.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // قد يتعرف Microsoft Word على المحتوى المذكور أعلاه باعتباره تاريخًا.
    // تستخدم العلامات الذكية خاصية "Element" لتعكس نوع البيانات التي تحتوي عليها.
    smartTag.Element = "date";

    // تقوم بعض أنواع العلامات الذكية بمعالجة محتوياتها بشكل أكبر في خصائص XML المخصصة.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // تعيين عنوان URI للعلامة الذكية إلى القيمة الافتراضية.
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

    // اطبع جميع العلامات الذكية في مستندنا باستخدام زائر المستند.
    doc.Accept(new SmartTagPrinter());

    // تدعم الإصدارات الأقدم من Microsoft Word العلامات الذكية.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    //استخدم طريقة "RemoveSmartTags" لإزالة كافة العلامات الذكية من المستند.
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
    /// يتم استدعاؤها عند مواجهة عقدة SmartTag في المستند.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند انتهاء زيارة عقدة SmartTag.
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

* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
