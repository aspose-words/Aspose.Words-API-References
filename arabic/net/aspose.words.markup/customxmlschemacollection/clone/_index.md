---
title: CustomXmlSchemaCollection.Clone
second_title: Aspose.Words لمراجع .NET API
description: CustomXmlSchemaCollection طريقة. عمل استنساخ عميق لهذا الكائن.
type: docs
weight: 50
url: /ar/net/aspose.words.markup/customxmlschemacollection/clone/
---
## CustomXmlSchemaCollection.Clone method

عمل استنساخ عميق لهذا الكائن.

```csharp
public CustomXmlSchemaCollection Clone()
```

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


