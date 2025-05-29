---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Markup.XmlMapping لربط علامات المستندات المنظمة بعناصر XML بسلاسة، مما يعزز تكامل بيانات مستندك.
type: docs
weight: 4790
url: /ar/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

يحدد المعلومات المستخدمة لإنشاء تعيين بين علامة المستند المهيكلة parent وعنصر XML المخزن داخل جزء بيانات XML مخصص في المستند.

لمعرفة المزيد، قم بزيارة[علامات المستند المنظم أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class XmlMapping
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | يعيد جزء بيانات XML المخصص الذي تم تعيين علامة المستند المنظم الرئيسي إليه. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | إرجاع`حقيقي` إذا تم تعيين علامة المستند المنظم الرئيسي بنجاح إلى بيانات XML. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | يعيد تعيينات بادئة مساحة اسم XML لتقييم[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | يحدد معرف بيانات XML المخصص لجزء بيانات XML المخصص والذي يجب استخدامه لتقييم[`XPath`](./xpath/) تعبير. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | يعيد تعبير XPath، الذي يتم تقييمه للعثور على node XML المخصصة التي تم تعيينها إلى علامة المستند المنظم الرئيسي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | يحذف تعيين المستند المنظم الرئيسي لبيانات XML. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | تعيين تعيين بين علامة المستند المنظم الرئيسي وعقدة XML لجزء بيانات XML مخصص. |

## أمثلة

يوضح كيفية تعيين تعيينات XML لأجزاء XML المخصصة.

```csharp
Document doc = new Document();

// قم بإنشاء جزء XML يحتوي على نص وإضافته إلى مجموعة CustomXmlPart الخاصة بالمستند.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// قم بإنشاء علامة مستند منظمة لعرض محتويات CustomXmlPart الخاص بنا.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// تعيين تعيين لعلامة مستندنا المهيكلة. سيُعلمك هذا التعيين
// علامة المستند المنظم لدينا لعرض جزء من محتويات نص جزء XML الذي يشير إليه XPath.
// في هذه الحالة، سيكون محتوى العنصر الثاني "<text>" للعنصر الأول "<root>": "عنصر النص رقم 2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'"، tag.XmlMapping.PrefixMappings);

// أضف علامة المستند المنظم إلى المستند لعرض المحتوى من الجزء المخصص لدينا.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
