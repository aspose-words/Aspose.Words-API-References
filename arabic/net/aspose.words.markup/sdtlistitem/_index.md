---
title: Class SdtListItem
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.SdtListItem فصل. يحدد هذا العنصر عنصر قائمة واحدًا داخل أحد الوالدينComboBox أوDropDownList علامة المستند المنظمة.
type: docs
weight: 4020
url: /ar/net/aspose.words.markup/sdtlistitem/
---
## SdtListItem class

يحدد هذا العنصر عنصر قائمة واحدًا داخل أحد الوالدينComboBox أوDropDownList علامة المستند المنظمة.

لمعرفة المزيد، قم بزيارة[علامات المستندات المنظمة أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class SdtListItem
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [SdtListItem](sdtlistitem/#constructor)(string) | تهيئة مثيل جديد لهذه الفئة. |
| [SdtListItem](sdtlistitem/#constructor_1)(string, string) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayText](../../aspose.words.markup/sdtlistitem/displaytext/) { get; } | يحصل على النص الذي سيتم عرضه في محتوى التشغيل بدلاً من[`Value`](./value/) محتويات السمة لعنصر القائمة هذا. |
| [Value](../../aspose.words.markup/sdtlistitem/value/) { get; } | يحصل على قيمة عنصر القائمة هذا. |

### أمثلة

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

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


