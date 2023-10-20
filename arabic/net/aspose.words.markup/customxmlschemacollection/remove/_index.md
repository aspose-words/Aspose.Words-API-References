---
title: CustomXmlSchemaCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words لـ .NET
description: CustomXmlSchemaCollection Remove طريقة. إزالة القيمة المحددة من المجموعة في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.markup/customxmlschemacollection/remove/
---
## CustomXmlSchemaCollection.Remove method

إزالة القيمة المحددة من المجموعة.

```csharp
public void Remove(string name)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | القيمة الحساسة لحالة الأحرف المطلوب إزالتها. |

## أمثلة

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

* class [CustomXmlSchemaCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
