---
title: CustomXmlProperty Class
linktitle: CustomXmlProperty
articleTitle: CustomXmlProperty
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Markup.CustomXmlProperty، المصممة لتبسيط إدارة سمات XML المخصصة وخصائص العلامات الذكية للتحكم المحسّن في المستندات.
type: docs
weight: 4630
url: /ar/net/aspose.words.markup/customxmlproperty/
---
## CustomXmlProperty class

يمثل سمة XML مخصصة واحدة أو خاصية علامة ذكية.

لمعرفة المزيد، قم بزيارة[علامات المستند المنظم أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class CustomXmlProperty
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CustomXmlProperty](customxmlproperty/)(*string, string, string*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Name](../../aspose.words.markup/customxmlproperty/name/) { get; } | يحدد اسم سمة XML المخصصة أو خاصية العلامة الذكية. |
| [Uri](../../aspose.words.markup/customxmlproperty/uri/) { get; set; } | يحصل على أو يعين اسم URI الخاص بمساحة اسم XML المخصصة أو خاصية العلامة الذكية. |
| [Value](../../aspose.words.markup/customxmlproperty/value/) { get; set; } | يحصل على قيمة سمة XML المخصصة أو خاصية العلامة الذكية أو يعينها. |

## ملاحظات

يستخدم كعنصر من[`CustomXmlPropertyCollection`](../customxmlpropertycollection/) مجموعة.

## أمثلة

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

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
