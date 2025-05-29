---
title: CustomXmlPartCollection Class
linktitle: CustomXmlPartCollection
articleTitle: CustomXmlPartCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Markup.CustomXmlPartCollection، الحل الأمثل لإدارة أجزاء XML المخصصة بكفاءة وبدون عناء.
type: docs
weight: 4620
url: /ar/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

يمثل مجموعة من أجزاء XML المخصصة. العناصر هي[`CustomXmlPart`](../customxmlpart/) الأشياء.

لمعرفة المزيد، قم بزيارة[علامات المستند المنظم أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class CustomXmlPartCollection : IEnumerable<CustomXmlPart>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CustomXmlPartCollection](customxmlpartcollection/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpartcollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | يحصل على عنصر أو يعينه في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(*[CustomXmlPart](../customxmlpart/)*) | يضيف عنصرًا إلى المجموعة. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(*string, string*) | ينشئ جزء XML جديدًا باستخدام XML المحدد ويضيفه إلى المجموعة. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | يزيل جميع العناصر من المجموعة. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | يقوم بعمل نسخة عميقة من هذه المجموعة وعناصرها. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(*string*) | يبحث عن جزء XML مخصص ويعيده حسب معرفه. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(*int*) | يزيل عنصرًا عند الفهرس المحدد. |

## ملاحظات

لا تحتاج عادةً إلى إنشاء مثيلات لهذه الفئة. يمكنك الوصول إلى بيانات XML المخصصة المخزنة في مستند عبر[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) ملكية.

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

* class [CustomXmlPart](../customxmlpart/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
