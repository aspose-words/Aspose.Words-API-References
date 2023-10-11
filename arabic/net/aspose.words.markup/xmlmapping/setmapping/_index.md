---
title: XmlMapping.SetMapping
second_title: Aspose.Words لمراجع .NET API
description: XmlMapping طريقة. يعين تعيينًا بين علامة المستند الهيكلية الأصلية وعقدة XML لجزء بيانات XML مخصص.
type: docs
weight: 70
url: /ar/net/aspose.words.markup/xmlmapping/setmapping/
---
## XmlMapping.SetMapping method

يعين تعيينًا بين علامة المستند الهيكلية الأصلية وعقدة XML لجزء بيانات XML مخصص.

```csharp
public bool SetMapping(CustomXmlPart customXmlPart, string xPath, string prefixMapping)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| customXmlPart | CustomXmlPart | جزء بيانات XML مخصص للتعيين إليه. |
| xPath | String | تعبير XPath للعثور على عقدة XML. |
| prefixMapping | String | تعيينات بادئة مساحة اسم XML لتقييم XPath. |

### قيمة الإرجاع

علامة تشير إلى ما إذا كان قد تم تعيين علامة المستند المنظمة الأصلية بنجاح إلى عقدة XML .

### أمثلة

يوضح كيفية إنشاء علامة مستند منظمة باستخدام بيانات XML المخصصة.

```csharp
Document doc = new Document();

// قم بإنشاء جزء XML يحتوي على بيانات وأضفه إلى مجموعة المستند.
// إذا قمنا بتمكين علامة التبويب "المطور" في Microsoft Word،
// يمكننا العثور على عناصر من هذه المجموعة في "جزء تعيين XML"، بالإضافة إلى بعض العناصر الافتراضية.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// فيما يلي طريقتان للإشارة إلى أجزاء XML.
// 1 - من خلال فهرس في مجموعة أجزاء XML المخصصة:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - بواسطة المعرف الدليلي:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// إضافة اقتران مخطط XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// انسخ جزءًا، ثم أدخله في المجموعة.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// كرر المجموعة واطبع محتويات كل جزء.
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

// استخدم طريقة "RemoveAt" لإزالة الجزء المستنسخ حسب الفهرس.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// انسخ مجموعة أجزاء XML، ثم استخدم طريقة "المسح" لإزالة جميع عناصرها مرة واحدة.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// أنشئ علامة مستند منظمة تعرض محتويات الجزء الخاص بنا وتدرجه في نص المستند.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### أنظر أيضا

* class [CustomXmlPart](../../customxmlpart/)
* class [XmlMapping](../)
* مساحة الاسم [Aspose.Words.Markup](../../xmlmapping/)
* المجسم [Aspose.Words](../../../)


