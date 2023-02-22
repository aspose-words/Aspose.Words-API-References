---
title: CustomXmlPart.DataChecksum
second_title: Aspose.Words لمراجع .NET API
description: CustomXmlPart ملكية. يحدد المجموع الاختباري لفحص التكرار الدوري CRC لملفData المحتوى .
type: docs
weight: 30
url: /ar/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

يحدد المجموع الاختباري لفحص التكرار الدوري (CRC) لملف[`Data`](../data/) المحتوى .

```csharp
public long DataChecksum { get; }
```

### أمثلة

يوضح كيفية حساب المجموع الاختباري في وقت التشغيل.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// يكون المجموع الاختباري للقراءة فقط ويتم حسابه باستخدام بيانات جزء بيانات XML المخصص المقابل.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// قمنا بتغيير XmlPart من العلامة ، وتم تحديث المجموع الاختباري في وقت التشغيل.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### أنظر أيضا

* class [CustomXmlPart](../)
* مساحة الاسم [Aspose.Words.Markup](../../customxmlpart/)
* المجسم [Aspose.Words](../../../)


