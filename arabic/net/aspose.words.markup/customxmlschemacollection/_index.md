---
title: CustomXmlSchemaCollection Class
linktitle: CustomXmlSchemaCollection
articleTitle: CustomXmlSchemaCollection
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Markup.CustomXmlSchemaCollection لإدارة مخططات XML المرتبطة بأجزاء XML المخصصة، وتحسين مرونة المستندات والتحكم فيها.
type: docs
weight: 4650
url: /ar/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

مجموعة من السلاسل التي تمثل مخططات XML المرتبطة بجزء XML مخصص.

لمعرفة المزيد، قم بزيارة[علامات المستند المنظم أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | يحصل على العنصر أو يعينه عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(*string*) | يضيف عنصرًا إلى المجموعة. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | يزيل جميع العناصر من المجموعة. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | يصنع استنساخًا عميقًا لهذا الكائن. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(*string*) | يعيد الفهرس المبني على الصفر للقيمة المحددة في المجموعة. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(*string*) | يزيل القيمة المحددة من المجموعة. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(*int*) | يزيل قيمة عند الفهرس المحدد. |

## ملاحظات

لا تُنشئ مثيلات لهذه الفئة. يمكنك الوصول إلى مجموعة مخططات XML لجزء XML مخصص عبر[`Schemas`](../customxmlpart/schemas/) ملكية.

## أمثلة

يوضح كيفية العمل مع مجموعة مخططات XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

//أضف ارتباط مخطط XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// استنساخ مجموعة ارتباطات مخطط XML الخاصة بجزء XML المخصص،
// ثم قم بإضافة زوج من المخططات الجديدة إلى الاستنساخ.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

//إحصاء المخططات وطباعة كل عنصر.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// فيما يلي ثلاث طرق لإزالة المخططات من المجموعة.
// 1 - إزالة مخطط حسب الفهرس:
schemas.RemoveAt(2);

// 2 - إزالة مخطط حسب القيمة:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - استخدم طريقة "المسح" لتفريغ المجموعة مرة واحدة.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
