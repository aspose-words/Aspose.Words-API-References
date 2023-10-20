---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Markup.XmlMapping فصل. يحدد المعلومات المستخدمة لتأسيس تعيين بين علامة المستند الهيكليةparent وعنصر XML المخزن داخل جزء بيانات XML مخصص في المستند في C#.
type: docs
weight: 4100
url: /ar/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

يحدد المعلومات المستخدمة لتأسيس تعيين بين علامة المستند الهيكليةparent وعنصر XML المخزن داخل جزء بيانات XML مخصص في المستند.

لمعرفة المزيد، قم بزيارة[علامات المستندات المنظمة أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class XmlMapping
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | إرجاع جزء بيانات XML المخصص الذي تم تعيين علامة المستند المنظمة الأصلية إليه. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | إرجاع`حقيقي` إذا تم تعيين علامة المستند المنظمة الأصلية بنجاح إلى بيانات XML. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | إرجاع تعيينات بادئة مساحة اسم XML لتقييم[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | يحدد معرف بيانات XML المخصص لجزء بيانات XML المخصص والذي يجب استخدامه لتقييم[`XPath`](./xpath/) التعبير. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | إرجاع تعبير XPath، الذي يتم تقييمه للعثور على عقدة XML المخصصة التي تم تعيينها لعلامة المستند الهيكلي الأصل. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | حذف تعيين المستند المنظم الأصلي إلى بيانات XML. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | يعين تعيينًا بين علامة المستند الهيكلية الأصلية وعقدة XML لجزء بيانات XML مخصص. |

## أمثلة

يوضح كيفية تعيين تعيينات XML لأجزاء XML المخصصة.

```csharp
Document doc = new Document();

// أنشئ جزءًا XML يحتوي على نص وأضفه إلى مجموعة CustomXmlPart الخاصة بالمستند.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>", 
    Encoding.UTF8.GetString(xmlPart.Data));

// أنشئ علامة مستند منظمة تعرض محتويات CustomXmlPart الخاصة بنا.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// قم بتعيين تعيين لعلامة المستند المنظمة الخاصة بنا. سوف يرشدك هذا التعيين
// علامة المستند المنظمة الخاصة بنا لعرض جزء من محتويات نص جزء XML الذي يشير إليه XPath.
// في هذه الحالة، ستكون محتويات "<text>" الثاني عنصر "<root>" الأول العنصر: "عنصر النص رقم 2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'"، tag.XmlMapping.PrefixMappings);

// أضف علامة المستند المنظمة إلى المستند لعرض المحتوى من الجزء المخصص لدينا.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
