---
title: Class CustomXmlPartCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.CustomXmlPartCollection فصل. يمثل مجموعة من أجزاء XML المخصصة. العناصرCustomXmlPart الكائنات .
type: docs
weight: 3690
url: /ar/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

يمثل مجموعة من أجزاء XML المخصصة. العناصر[`CustomXmlPart`](../customxmlpart/) الكائنات .

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
| [Count](../../aspose.words.markup/customxmlpartcollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | الحصول على أو تعيين عنصر في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(CustomXmlPart) | يضيف عنصرًا إلى المجموعة . |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(string, string) | إنشاء جزء XML جديد باستخدام XML المحدد وإضافته إلى المجموعة. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | يزيل كل العناصر من المجموعة. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | عمل نسخة عميقة من هذه المجموعة وعناصرها. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(string) | البحث عن جزء XML المخصص وإرجاعه بواسطة معرفه. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر في المجموعة. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(int) | إزالة عنصر في الفهرس المحدد . |

### ملاحظات

لا تحتاج عادةً إلى إنشاء نسخ من هذه الفئة. يمكنك الوصول إلى بيانات XML المخصصة المخزنة في مستند عبر[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) منشأه.

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

* class [CustomXmlPart](../customxmlpart/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


