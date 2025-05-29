---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم خاصية StructuredDocumentTagRangeStart XmlMapping بربط نطاق علامات المستند الخاص بك ببيانات XML المخصصة، مما يعزز تكامل المستند.
type: docs
weight: 190
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

يحصل على كائن يمثل تعيين نطاق علامة المستند المنظم هذا إلى XML data في جزء XML مخصص من المستند الحالي.

```csharp
public XmlMapping XmlMapping { get; }
```

## ملاحظات

يمكنك استخدام[`SetMapping`](../../xmlmapping/setmapping/) طريقة هذا الكائن لتعيين نطاق علامة مستند منظم إلى بيانات XML.

## أمثلة

يوضح كيفية تعيين تعيينات XML لبداية النطاق لعلامة مستند منظمة.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// قم بإنشاء جزء XML يحتوي على نص وإضافته إلى مجموعة CustomXmlPart الخاصة بالمستند.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// قم بإنشاء علامة مستند منظمة لعرض محتويات CustomXmlPart في المستند.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// إذا قمنا بتعيين تعيين لعلامة المستند المنظم لدينا،
// سيتم عرض جزء فقط من CustomXmlPart الذي يشير إليه XPath.
// سيشير هذا XPath إلى محتوى العنصر الثاني "<text>" من العنصر الأول "<root>" في CustomXmlPart الخاص بنا.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### أنظر أيضا

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
