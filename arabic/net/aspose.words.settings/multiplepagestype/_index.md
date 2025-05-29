---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Settings.MultiplePagesType enum لخيارات طباعة مستندات فعّالة. حسّن سير عملك بإعدادات طباعة مرنة!
type: docs
weight: 6700
url: /ar/net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

يحدد كيفية طباعة المستند.

```csharp
public enum MultiplePagesType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Normal | `0` | الطباعة العادية، لا توجد صفحات متعددة محددة. |
| MirrorMargins | `1` | تبديل الهوامش اليمنى واليسرى على الصفحات المتقابلة. |
| TwoPagesPerSheet | `2` | تطبع صفحتين لكل ورقة. |
| BookFoldPrinting | `3` | يحدد ما إذا كان سيتم طباعة المستند ككتاب مطوي. |
| BookFoldPrintingReverse | `4` | يحدد ما إذا كان سيتم طباعة المستند ككتاب مطوي عكسيًا. |
| Default | `0` | القيمة الافتراضية هيNormal |

## أمثلة

يوضح كيفية تكوين مستند يمكن طباعته ككتاب مطوي.

```csharp
Document doc = new Document();

//إدراج نص يمتد على 16 صفحة.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// قم بتكوين خاصية "PageSetup" في القسم الأول لطباعة المستند في شكل كتاب مطوي.
// عندما نقوم بطباعة هذه الوثيقة على كلا الجانبين، يمكننا أخذ الصفحات لتكديسها
// ثم اطوِها كلها من المنتصف دفعةً واحدة. سيُطوى محتوى المستند ككتاب.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// يمكننا فقط تحديد عدد الأوراق بمضاعفات 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
