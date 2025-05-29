---
title: CompositeNode.CreateNavigator
linktitle: CreateNavigator
articleTitle: CreateNavigator
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة CompositeNode CreateNavigator للتنقل بين العقد وقراءتها بسهولة، مما يعزز تجربة التنقل بين البيانات لديك.
type: docs
weight: 90
url: /ar/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

## أمثلة

يوضح كيفية إنشاء XPathNavigator، ثم استخدامه للتنقل بين العقد وقراءتها.

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
        // الجسم، والفقرة الأولى كعقد، حيث يكون كل منهما طفلًا وحيدًا للعقدة السابقة.
        //يمكننا إضافة المزيد لإعطاء الشجرة بعض الفروع حتى يتمكن المستكشف من التنقل خلالها.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // استخدم المستعرض الخاص بنا لطباعة خريطة لجميع العقد الموجودة في المستند على وحدة التحكم.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// يجتاز جميع أبناء العقدة المركبة ويقوم برسم البنية بأسلوب شجرة الدليل.
/// تشير كمية المسافة البادئة إلى العمق بالنسبة للعقدة الأولية.
/// يطبع محتويات النص الخاصة بالعقدة الحالية فقط إذا كانت تشغيلًا.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
