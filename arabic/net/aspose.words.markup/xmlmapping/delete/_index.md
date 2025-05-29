---
title: XmlMapping.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words لـ .NET
description: أزل تعيينات بيانات XML بسهولة باستخدام طريقة حذف XmlMapping. بسّط مستنداتك المهيكلة لتحسين الكفاءة والتنظيم.
type: docs
weight: 60
url: /ar/net/aspose.words.markup/xmlmapping/delete/
---
## XmlMapping.Delete method

يحذف تعيين المستند المنظم الرئيسي لبيانات XML.

```csharp
public void Delete()
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

* class [XmlMapping](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
