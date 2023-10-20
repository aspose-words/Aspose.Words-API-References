---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words لـ .NET
description: PageSetup SheetsPerBooklet ملكية. إرجاع أو تعيين عدد الصفحات التي سيتم تضمينها في كل كتيب في C#.
type: docs
weight: 400
url: /ar/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

إرجاع أو تعيين عدد الصفحات التي سيتم تضمينها في كل كتيب.

```csharp
public int SheetsPerBooklet { get; set; }
```

## أمثلة

يوضح كيفية تكوين مستند يمكن طباعته كطي كتاب.

```csharp
Document doc = new Document();

// أدخل نصًا يمتد إلى 16 صفحة.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// قم بتكوين خاصية "PageSetup" للقسم الأول لطباعة المستند على شكل طية كتاب.
// عندما نطبع هذه الوثيقة على كلا الجانبين، يمكننا أخذ الصفحات لتكديسها
// وقم بطيها جميعًا في المنتصف مرة واحدة. سوف تصطف محتويات المستند في طية الكتاب.
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
