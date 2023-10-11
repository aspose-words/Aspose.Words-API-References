---
title: CompositeNode.CreateNavigator
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode طريقة. إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها.
type: docs
weight: 90
url: /ar/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

### أمثلة

يوضح كيفية إنشاء XPathNavigator، ثم استخدامه لاجتياز العقد وقراءتها.

```csharp
public void NodeXPathNavigator()
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // تحتوي شجرة المستندات على المستند، القسم الأول،
        // النص والفقرة الأولى كعقد، حيث تكون كل منهما فرعًا وحيدًا للفقرة السابقة.
        // يمكننا إضافة المزيد لإعطاء الشجرة بعض الفروع ليتمكن الملاح من اجتيازها.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // استخدم متصفحنا لطباعة خريطة لجميع العقد الموجودة في المستند إلى وحدة التحكم.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// يجتاز كافة العناصر الفرعية للعقدة المركبة ويرسم خريطة للبنية بأسلوب شجرة الدليل.
/// يشير مقدار المسافة البادئة للمساحة إلى العمق بالنسبة للعقدة الأولية.
/// يطبع محتويات النص للعقدة الحالية فقط إذا كانت قيد التشغيل.
/// </summary>
private static void MapDocument(XPathNavigator navigator, StringBuilder stringBuilder, int depth)
{
    do
    {
        stringBuilder.Append(' ', depth);
        stringBuilder.Append(navigator.Name + ": ");

        if (navigator.Name == "Run")
        {
            stringBuilder.Append(navigator.Value);
        }

        stringBuilder.Append('\n');

        if (navigator.HasChildren)
        {
            navigator.MoveToFirstChild();
            MapDocument(navigator, stringBuilder, depth + 1);
            navigator.MoveToParent();
        }
    } while (navigator.MoveToNext());
}
```

### أنظر أيضا

* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


