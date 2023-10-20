---
title: SdtListItemCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: SdtListItemCollection Item ملكية. إرجاع أSdtListItem كائن بالنظر إلى فهرسه الصفري في المجموعة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.markup/sdtlistitemcollection/item/
---
## SdtListItemCollection indexer

إرجاع أ[`SdtListItem`](../../sdtlistitem/) كائن بالنظر إلى فهرسه الصفري في المجموعة.

```csharp
public SdtListItem this[int index] { get; }
```

## أمثلة

يوضح كيفية العمل مع علامات المستندات المنظمة ذات القائمة المنسدلة.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// علامة المستند المنظمة للقائمة المنسدلة هي نموذج يسمح للمستخدم بذلك
// حدد خيارًا من القائمة بالنقر بزر الماوس الأيسر وفتح النموذج في Microsoft Word.
// تحتوي الخاصية "ListItems" على كافة عناصر القائمة، وكل عنصر في القائمة هو "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// أضف 3 عناصر أخرى إلى القائمة. قم بتهيئة هذه العناصر باستخدام مُنشئ مختلف للعنصر الأول
// لعرض سلاسل مختلفة عن قيمها.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// تعرض القائمة المنسدلة العنصر الأول. قم بتعيين عنصر قائمة مختلف إلى "SelectedValue" لعرضه.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// تعداد المجموعة وطباعة كل عنصر.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // إزالة عنصر القائمة الأخير.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// بما أن عنصر التحكم المنسدل الخاص بنا تم ضبطه لعرض العنصر المحذوف افتراضيًا، فامنحه عنصرًا موجودًا لعرضه.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// استخدم طريقة "مسح" لإفراغ مجموعة العناصر المنسدلة بالكامل مرة واحدة.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### أنظر أيضا

* class [SdtListItem](../../sdtlistitem/)
* class [SdtListItemCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
