---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words لـ .NET
description: CustomXmlPart DataChecksum ملكية. يحدد المجموع الاختباري لفحص التكرار الدوري CRC لـData المحتوى في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

يحدد المجموع الاختباري لفحص التكرار الدوري (CRC) لـ[`Data`](../data/) المحتوى.

```csharp
public long DataChecksum { get; }
```

## أمثلة

يوضح كيفية حساب المجموع الاختباري في وقت التشغيل.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// المجموع الاختباري للقراءة فقط ويتم حسابه باستخدام بيانات جزء بيانات XML المخصص المقابل.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// قمنا بتغيير XmlPart للعلامة، وتم تحديث المجموع الاختباري في وقت التشغيل.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### أنظر أيضا

* class [CustomXmlPart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
