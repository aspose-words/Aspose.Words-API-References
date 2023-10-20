---
title: XmlMapping.XPath
linktitle: XPath
articleTitle: XPath
second_title: Aspose.Words لـ .NET
description: XmlMapping XPath ملكية. إرجاع تعبير XPath الذي يتم تقييمه للعثور على عقدة XML المخصصة التي تم تعيينها لعلامة المستند الهيكلي الأصل في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.markup/xmlmapping/xpath/
---
## XmlMapping.XPath property

إرجاع تعبير XPath، الذي يتم تقييمه للعثور على عقدة XML المخصصة التي تم تعيينها لعلامة المستند الهيكلي الأصل.

```csharp
public string XPath { get; }
```

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

* class [XmlMapping](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
