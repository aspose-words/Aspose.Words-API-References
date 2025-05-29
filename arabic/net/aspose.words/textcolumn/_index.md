---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.TextColumn لإدارة أعمدة النص في مستنداتك. يمكنك الوصول بسهولة إلى كل عمود في قسم النص وتخصيصه.
type: docs
weight: 7240
url: /ar/net/aspose.words/textcolumn/
---
## TextColumn class

يمثل عمود نص واحد.`TextColumn` هو عضو في[`TextColumnCollection`](../textcolumncollection/) المجموعة. `TextColumn`تتضمن المجموعة جميع الأعمدة الموجودة في قسم من المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأقسام](https://docs.aspose.com/words/net/working-with-sections/) مقالة توثيقية.

```csharp
public class TextColumn
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | يُحدِّد المسافة بين هذا العمود والعمود التالي بالنقاط، أو يُحدِّدها. غير مطلوب للعمود الأخير. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | يحصل على عرض عمود النص بالنقاط أو يعينه. |

## ملاحظات

`TextColumn` تُستخدم الكائنات فقط لتحديد أعمدة بعرض ومسافة مخصصة. إذا أردت أن تكون أعمدة المستند متساوية العرض، فاضبط TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) ل`حقيقي`.

عندما يكون هناك جديد`TextColumn` يتم إنشاؤه بحيث يكون عرضه وتباعده مضبوطين على الصفر.

## أمثلة

يوضح كيفية إنشاء أعمدة متباعدة بشكل غير متساوٍ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// تحديد مقدار المساحة المتوفرة لدينا لترتيب الأعمدة.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// تعيين العمود الأول ليكون ضيقًا.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// قم بتعيين العمود الثاني ليشغل المساحة المتبقية المتوفرة ضمن هوامش الصفحة.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
