---
title: Class CustomXmlSchemaCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.CustomXmlSchemaCollection فصل. مجموعة من السلاسل التي تمثل مخططات XML المرتبطة بجزء XML مخصص.
type: docs
weight: 3960
url: /ar/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

مجموعة من السلاسل التي تمثل مخططات XML المرتبطة بجزء XML مخصص.

لمعرفة المزيد، قم بزيارة[علامات المستندات المنظمة أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | الحصول على العنصر أو تعيينه في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(string) | إضافة عنصر إلى المجموعة. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | إزالة كافة العناصر من المجموعة. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | إجراء استنساخ عميق لهذا الكائن. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(string) | إرجاع الفهرس الصفري للقيمة المحددة في المجموعة. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(string) | إزالة القيمة المحددة من المجموعة. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(int) | إزالة قيمة في الفهرس المحدد. |

### ملاحظات

لا تقم بإنشاء مثيلات هذه الفئة. يمكنك الوصول إلى مجموعة مخططات XML الخاصة بـ XML Part عبر ملف[`Schemas`](../customxmlpart/schemas/) ملكية.

### أمثلة

يوضح كيفية العمل مع مجموعة مخططات XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// إضافة اقتران مخطط XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// استنساخ مجموعة اقتران مخطط XML لجزء XML المخصص،
// ثم قم بإضافة اثنين من المخططات الجديدة إلى النسخة.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// قم بتعداد المخططات وطباعة كل عنصر.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// فيما يلي ثلاث طرق لإزالة المخططات من المجموعة.
// 1 - إزالة المخطط حسب الفهرس:
schemas.RemoveAt(2);

// 2 - إزالة المخطط حسب القيمة:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - استخدم طريقة "المسح" لإفراغ المجموعة مرة واحدة.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


