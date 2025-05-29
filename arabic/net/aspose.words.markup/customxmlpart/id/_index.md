---
title: CustomXmlPart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة خاصية CustomXmlPart Id لتحديد أجزاء XML وتخصيصها بسهولة في مستندات OOXML الخاصة بك لتحسين إدارة المستندات.
type: docs
weight: 40
url: /ar/net/aspose.words.markup/customxmlpart/id/
---
## CustomXmlPart.Id property

يحصل على السلسلة التي تحدد جزء XML المخصص هذا داخل مستند OOXML أو يعينها.

```csharp
public string Id { get; set; }
```

## ملاحظات

يُحدد معيار ISO/IEC 29500 أن هذه القيمة هي مُعرِّف فريد عالمي (GUID)، ولكن الإصدارات القديمة من Microsoft Word كانت تسمح باستخدام سلسلة نصية any هنا. يقوم Aspose.Words بالشيء نفسه مع تنسيق ECMA-376. ولكن تجدر الإشارة إلى أن Microsoft Word Online لا يفتح مستندًا مُنشأً بقيمة غير مُعرِّف فريد عالمي (GUID). لذا، يُفضَّل استخدام مُعرِّف فريد عالمي (GUID) لهذه الخاصية.

يجب أن تكون القيمة الصالحة عبارة عن معرف فريد بين جميع أجزاء بيانات XML المخصصة في هذا المستند.

القيمة الافتراضية هي سلسلة فارغة. لا يمكن استخدام القيمة`باطل`.

## أمثلة

يوضح كيفية إنشاء علامة مستند منظمة باستخدام بيانات XML مخصصة.

```csharp
Document doc = new Document();

// إنشاء جزء XML يحتوي على البيانات وإضافته إلى مجموعة المستند.
// إذا قمنا بتمكين علامة التبويب "المطور" في Microsoft Word،
// يمكننا العثور على عناصر من هذه المجموعة في "جزء تعيين XML"، إلى جانب بعض العناصر الافتراضية.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// فيما يلي طريقتان للإشارة إلى أجزاء XML.
// 1 - حسب الفهرس في مجموعة أجزاء XML المخصصة:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - حسب GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

//أضف ارتباط مخطط XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

//استنساخ جزء، ثم إدراجه في المجموعة.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// قم بالتكرار خلال المجموعة وطباعة محتويات كل جزء.
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

//استخدم طريقة "RemoveAt" لإزالة الجزء المستنسخ حسب الفهرس.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// استنساخ مجموعة أجزاء XML، ثم استخدام طريقة "مسح" لإزالة كافة عناصرها مرة واحدة.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// قم بإنشاء علامة مستند منظمة لعرض محتويات الجزء الخاص بنا وإدراجها في نص المستند.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### أنظر أيضا

* class [CustomXmlPart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
