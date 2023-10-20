---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Markup.CustomXmlPart فصل. يمثل جزءًا مخصصًا لتخزين بيانات XML بيانات XML مخصصة داخل الحزمة في C#.
type: docs
weight: 3920
url: /ar/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

يمثل جزءًا مخصصًا لتخزين بيانات XML (بيانات XML مخصصة داخل الحزمة).

لمعرفة المزيد، قم بزيارة[علامات المستندات المنظمة أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class CustomXmlPart
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CustomXmlPart](customxmlpart/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | الحصول على محتوى XML الخاص بجزء تخزين بيانات XML المخصص هذا أو تعيينه. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | يحدد المجموع الاختباري لفحص التكرار الدوري (CRC) لـ[`Data`](./data/) المحتوى. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | الحصول على أو تعيين السلسلة التي تحدد جزء XML المخصص هذا داخل مستند OOXML. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | يحدد مجموعة مخططات XML المرتبطة بجزء XML المخصص هذا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | يقوم بإنشاء نسخة "عميقة بما فيه الكفاية" من الكائن. لا يكرر بايتات ملف[`Data`](./data/) القيمة. |

## ملاحظات

يمكن أن يحتوي مستند DOCX أو DOC على جزء واحد أو أكثر من أجزاء تخزين بيانات XML المخصصة. يحافظ Aspose.Words على ويسمح بإنشاء واستخراج بيانات XML المخصصة عبر[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) مجموعة.

## أمثلة

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

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
