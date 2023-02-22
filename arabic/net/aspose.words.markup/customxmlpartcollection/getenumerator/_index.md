---
title: CustomXmlPartCollection.GetEnumerator
second_title: Aspose.Words لمراجع .NET API
description: CustomXmlPartCollection طريقة. إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر في المجموعة.
type: docs
weight: 80
url: /ar/net/aspose.words.markup/customxmlpartcollection/getenumerator/
---
## CustomXmlPartCollection.GetEnumerator method

إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر في المجموعة.

```csharp
public IEnumerator<CustomXmlPart> GetEnumerator()
```

### أمثلة

يوضح كيفية إنشاء علامة مستند منظم ببيانات XML مخصصة.

```csharp
Document doc = new Document();

// إنشاء جزء XML يحتوي على بيانات وإضافته إلى مجموعة المستند.
// إذا قمنا بتمكين علامة التبويب "المطور" في Microsoft Word ،
// يمكننا العثور على عناصر من هذه المجموعة في "جزء تعيين XML" ، جنبًا إلى جنب مع بعض العناصر الافتراضية.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// فيما يلي طريقتان للإشارة إلى أجزاء XML.
// 1 - بواسطة فهرس في مجموعة أجزاء XML المخصصة:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - بواسطة GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// إضافة اقتران مخطط XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema ") ;

// استنساخ جزء ، ثم أدخله في المجموعة.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// تكرار خلال المجموعة وطباعة محتويات كل جزء.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// استخدم طريقة "RemoveAt" لإزالة الجزء المستنسخ بالفهرس.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// استنساخ مجموعة أجزاء XML ، ثم استخدم طريقة "Clear" لإزالة جميع عناصرها مرة واحدة.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// قم بإنشاء علامة مستند منظم تعرض محتويات الجزء الخاص بنا وإدراجها في نص المستند.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### أنظر أيضا

* class [CustomXmlPart](../../customxmlpart/)
* class [CustomXmlPartCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../customxmlpartcollection/)
* المجسم [Aspose.Words](../../../)


