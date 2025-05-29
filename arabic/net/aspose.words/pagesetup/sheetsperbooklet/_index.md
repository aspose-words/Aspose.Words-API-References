---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup SheetsPerBooklet لإدارة عدد صفحات الكتيب بسهولة، مما يعزز تخطيط مستندك وكفاءة الطباعة.
type: docs
weight: 400
url: /ar/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

يقوم بإرجاع أو تعيين عدد الصفحات التي سيتم تضمينها في كل كتيب.

```csharp
public int SheetsPerBooklet { get; set; }
```

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

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
