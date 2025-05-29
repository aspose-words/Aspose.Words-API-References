---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CustomXmlPart DataChecksum، التي تضمن سلامة البيانات من خلال مجموع تدقيق CRC موثوق لمحتوى XML. حسّن موثوقية بياناتك!
type: docs
weight: 30
url: /ar/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

يحدد مجموع اختبار التكرار الدوري (CRC) لـ[`Data`](../data/) المحتوى.

```csharp
public long DataChecksum { get; }
```

## أمثلة

يُظهر كيفية حساب المبلغ الاختباري في وقت التشغيل.

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

// لقد قمنا بتغيير XmlPart للعلامة، وتم تحديث المجموع الاختباري في وقت التشغيل.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### أنظر أيضا

* class [CustomXmlPart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
