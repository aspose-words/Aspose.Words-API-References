---
title: ImportFormatOptions.KeepSourceNumbering
linktitle: KeepSourceNumbering
articleTitle: KeepSourceNumbering
second_title: Aspose.Words لـ .NET
description: تحكم في ترقيم المستندات باستخدام خاصية KeepSourceNumbering في ImportFormatOptions. أدر التعارضات بسهولة لضمان عمليات استيراد سلسة. الافتراضي خطأ.
type: docs
weight: 60
url: /ar/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

يحصل على قيمة منطقية أو يعينها لتحديد كيفية استيراد الترقيم عندما يتعارض في المستندات المصدر و الوجهة. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

## أمثلة

يوضح كيفية حل التعارض عند استيراد المستندات التي تحتوي على قوائم بنفس معرف تعريف القائمة.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// اضبط خاصية "KeepSourceNumbering" على "true" لتطبيق معرف تعريف قائمة مختلف
// إلى الأنماط المتطابقة مثل Aspose.Words التي يستوردها إلى المستندات الوجهة.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

يوضح كيفية استيراد مستند بقوائم مرقمة.

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// إذا كان هناك تعارض بين أنماط القائمة، قم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// قم بتعيين خاصية "KeepSourceNumbering" إلى "false" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "true" لاستيراد جميع البيانات المتضاربة
// ترقيم نمط القائمة بنفس المظهر الذي كان عليه في المستند المصدر.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

يوضح كيفية حل تعارضات ترقيم القائمة في المستندات المصدر والوجهة.

```csharp
// افتح مستندًا يحتوي على مخطط ترقيم قائمة مخصص، ثم استنسخه.
// نظرًا لأن كلاهما لهما نفس تنسيق الترقيم، فسوف تتعارض التنسيقات إذا قمنا باستيراد مستند واحد إلى الآخر.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// عندما نقوم باستيراد نسخة من المستند إلى المستند الأصلي ثم إضافته،
// ثم سيتم دمج القائمتين اللتين لهما نفس تنسيق القائمة.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" إلى "false"، فسيتم استنساخ القائمة من المستند
// الذي نضيفه إلى الأصل سيحمل ترقيم القائمة التي نضيفه إليها.
// سيؤدي هذا إلى دمج القائمتين في قائمة واحدة بشكل فعال.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" إلى "true"، فسيتم استنساخ المستند
 // ستحافظ القائمة على ترقيمها الأصلي، مما يجعل القائمتين تظهران كقوائم منفصلة.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### أنظر أيضا

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
