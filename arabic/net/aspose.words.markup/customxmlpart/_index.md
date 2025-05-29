---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Markup.CustomXmlPart لإدارة فعّالة لتخزين بيانات XML المُخصّصة ضمن الحزم. حسّن معالجة مستنداتك اليوم!
type: docs
weight: 4610
url: /ar/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

يمثل جزء تخزين بيانات XML مخصص (بيانات XML مخصصة داخل حزمة).

لمعرفة المزيد، قم بزيارة[علامات المستند المنظم أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

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
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | يحصل على محتوى XML الخاص بجزء تخزين بيانات XML المخصص هذا أو يعينه. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | يحدد مجموع اختبار التكرار الدوري (CRC) لـ[`Data`](./data/) المحتوى. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | يحصل على السلسلة التي تحدد جزء XML المخصص هذا داخل مستند OOXML أو يعينها. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | يحدد مجموعة مخططات XML المرتبطة بهذا الجزء المخصص من XML. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | يقوم بعمل نسخة "عميقة بدرجة كافية" من الكائن. لا يقوم بتكرار بايتات الكائن[`Data`](./data/) القيمة. |

## ملاحظات

يمكن أن يحتوي مستند DOCX أو DOC على جزء أو أكثر من أجزاء تخزين بيانات XML المخصصة. يحافظ Aspose.Words على بيانات XML المخصصة، ويسمح بإنشاء بيانات XML مخصصة واستخراجها عبر[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) مجموعة.

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

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
