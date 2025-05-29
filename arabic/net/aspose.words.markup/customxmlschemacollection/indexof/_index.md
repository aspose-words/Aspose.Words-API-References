---
title: CustomXmlSchemaCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة CustomXmlSchemaCollection IndexOf، التي تعمل بكفاءة على العثور على الفهرس المبني على الصفر لأي قيمة محددة في مجموعة XML الخاصة بك.
type: docs
weight: 70
url: /ar/net/aspose.words.markup/customxmlschemacollection/indexof/
---
## CustomXmlSchemaCollection.IndexOf method

يعيد الفهرس المبني على الصفر للقيمة المحددة في المجموعة.

```csharp
public int IndexOf(string value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| value | String | القيمة الحساسة لحالة الأحرف التي يجب تحديد موقعها. |

### قيمة الإرجاع

الفهرس صفري. قيمة سلبية في حال عدم العثور عليه.

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

* class [CustomXmlSchemaCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
