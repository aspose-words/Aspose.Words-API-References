---
title: SdtListItemCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words لـ .NET
description: احذف عنصر قائمة بسهولة حسب الفهرس باستخدام طريقة SdtListItemCollection RemoveAt. بسّط إدارة بياناتك اليوم!
type: docs
weight: 70
url: /ar/net/aspose.words.markup/sdtlistitemcollection/removeat/
---
## SdtListItemCollection.RemoveAt method

يزيل عنصر القائمة عند الفهرس المحدد.

```csharp
public void RemoveAt(int index)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | الفهرس المبني على الصفر للعنصر الذي سيتم إزالته. |

## أمثلة

يوضح كيفية العمل مع علامات المستند المنظمة في القائمة المنسدلة.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// علامة المستند المنظمة القائمة المنسدلة هي نموذج يسمح للمستخدم بـ
// حدد خيارًا من القائمة عن طريق النقر بزر الماوس الأيسر وفتح النموذج في Microsoft Word.
// تحتوي خاصية "ListItems" على جميع عناصر القائمة، وكل عنصر قائمة هو "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// أضف ثلاثة عناصر إضافية إلى القائمة. هجّر هذه العناصر باستخدام مُنشئ مختلف عن العنصر الأول.
// لعرض السلاسل التي تختلف عن قيمها.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// تعرض القائمة المنسدلة العنصر الأول. عيّن عنصرًا آخر إلى "القيمة المحددة" لعرضه.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// قم بإحصاء المجموعة وطباعة كل عنصر.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // قم بإزالة العنصر الأخير من القائمة.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// بما أن عنصر التحكم في القائمة المنسدلة لدينا مضبوط لعرض العنصر الذي تمت إزالته بشكل افتراضي، فامنحه عنصرًا موجودًا لعرضه.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

//استخدم طريقة "المسح" لتفريغ مجموعة العناصر المنسدلة بالكامل مرة واحدة.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### أنظر أيضا

* class [SdtListItemCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
