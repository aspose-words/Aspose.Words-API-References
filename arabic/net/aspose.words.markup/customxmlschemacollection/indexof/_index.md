---
title: CustomXmlSchemaCollection.IndexOf
second_title: Aspose.Words لمراجع .NET API
description: CustomXmlSchemaCollection طريقة. إرجاع الفهرس الصفري للقيمة المحددة في المجموعة.
type: docs
weight: 70
url: /ar/net/aspose.words.markup/customxmlschemacollection/indexof/
---
## CustomXmlSchemaCollection.IndexOf method

إرجاع الفهرس الصفري للقيمة المحددة في المجموعة.

```csharp
public int IndexOf(string value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| value | String | القيمة الحساسة لحالة الأحرف المطلوب تحديدها. |

### قيمة الإرجاع

المؤشر الصفري. القيمة السلبية إذا لم يتم العثور عليها.

### أمثلة

يوضح كيفية العمل مع مجموعة مخطط XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// إضافة اقتران مخطط XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema ") ;

// استنساخ مجموعة اقتران مخطط XML لجزء XML المخصص ،
// ثم قم بإضافة بعض المخططات الجديدة إلى النسخة.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance ") ;
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType ") ;

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType ")) ;

// عد المخططات واطبع كل عنصر.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// فيما يلي ثلاث طرق لإزالة المخططات من المجموعة.
// 1 - إزالة مخطط قاعدة بيانات بواسطة الفهرس:
schemas.RemoveAt(2);

// 2 - إزالة مخطط قاعدة بيانات حسب القيمة:
schemas.Remove("http://www.w3.org/2001/XMLSchema ") ;

// 3 - استخدم طريقة "Clear" لتفريغ المجموعة مرة واحدة.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### أنظر أيضا

* class [CustomXmlSchemaCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../customxmlschemacollection/)
* المجسم [Aspose.Words](../../../)


