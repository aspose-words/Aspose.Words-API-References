---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTagRangeStart XmlMapping ملكية. الحصول على كائن يمثل تعيين نطاق علامات المستند المنظم هذا إلى بيانات XML في جزء XML مخصص من المستند الحالي في C#.
type: docs
weight: 180
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

الحصول على كائن يمثل تعيين نطاق علامات المستند المنظم هذا إلى بيانات XML في جزء XML مخصص من المستند الحالي.

```csharp
public XmlMapping XmlMapping { get; }
```

## ملاحظات

يمكنك استخدام[`SetMapping`](../../xmlmapping/setmapping/) طريقة الكائن this لتعيين نطاق علامات المستند المنظم إلى بيانات XML.

## أمثلة

يوضح كيفية تعيين تعيينات XML لنطاق بداية علامة المستند المنظمة.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// أنشئ جزءًا XML يحتوي على نص وأضفه إلى مجموعة CustomXmlPart الخاصة بالمستند.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// أنشئ علامة مستند منظمة تعرض محتويات CustomXmlPart في المستند.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// إذا قمنا بتعيين تعيين لعلامة الوثيقة المنظمة لدينا،
// سيعرض فقط جزء من CustomXmlPart الذي يشير إليه XPath.
// سيشير XPath هذا إلى المحتويات الثانية "<text>" عنصر "<root>" الأول عنصر CustomXmlPart الخاص بنا.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### أنظر أيضا

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
