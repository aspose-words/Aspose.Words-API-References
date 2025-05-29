---
title: XmlMapping.CustomXmlPart
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية XmlMapping CustomXmlPart، التي تربط علامات المستند المنظمة بأجزاء بيانات XML المخصصة لتحسين تكامل المستند.
type: docs
weight: 10
url: /ar/net/aspose.words.markup/xmlmapping/customxmlpart/
---
## XmlMapping.CustomXmlPart property

يعيد جزء بيانات XML المخصص الذي تم تعيين علامة المستند المنظم الرئيسي إليه.

```csharp
public CustomXmlPart CustomXmlPart { get; }
```

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

* class [CustomXmlPart](../../customxmlpart/)
* class [XmlMapping](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
