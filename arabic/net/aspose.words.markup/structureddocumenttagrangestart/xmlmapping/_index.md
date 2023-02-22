---
title: StructuredDocumentTagRangeStart.XmlMapping
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTagRangeStart ملكية. الحصول على كائن يمثل تعيين نطاق علامة المستند المهيكلة هذا إلى بيانات XML في جزء XML مخصص من المستند الحالي.
type: docs
weight: 180
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

الحصول على كائن يمثل تعيين نطاق علامة المستند المهيكلة هذا إلى بيانات XML في جزء XML مخصص من المستند الحالي.

```csharp
public XmlMapping XmlMapping { get; }
```

### ملاحظات

يمكنك استخدام ملف[`SetMapping`](../../xmlmapping/setmapping/) طريقة الكائن this لتعيين نطاق علامة مستند منظم إلى بيانات XML.

### أمثلة

يوضح كيفية تعيين تعيينات XML لبداية النطاق لعلامة مستند منظم.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// إنشاء جزء XML يحتوي على نص وإضافته إلى مجموعة CustomXmlPart الخاصة بالمستند.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// قم بإنشاء علامة مستند منظم تعرض محتويات CustomXmlPart في المستند.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// إذا قمنا بتعيين تعيين لعلامة المستند المنظمة الخاصة بنا ،
// سيعرض فقط جزءًا من CustomXmlPart الذي يشير إليه XPath.
// سيشير XPath هذا إلى المحتويات ثانيًا "< text >" عنصر أول "< root >" عنصر CustomXmlPart الخاص بنا.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### أنظر أيضا

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* المجسم [Aspose.Words](../../../)


