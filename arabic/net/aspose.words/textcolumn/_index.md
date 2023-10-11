---
title: Class TextColumn
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.TextColumn فصل. يمثل عمود نص واحد.TextColumn هو عضو فيTextColumnCollection المجموعة. الTextColumn تتضمن المجموعة جميع الأعمدة الموجودة في قسم من المستند.
type: docs
weight: 6390
url: /ar/net/aspose.words/textcolumn/
---
## TextColumn class

يمثل عمود نص واحد.`TextColumn` هو عضو في[`TextColumnCollection`](../textcolumncollection/) المجموعة. ال`TextColumn` تتضمن المجموعة جميع الأعمدة الموجودة في قسم من المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأقسام](https://docs.aspose.com/words/net/working-with-sections/) مقالة توثيقية.

```csharp
public class TextColumn
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | الحصول على أو تعيين المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | الحصول على أو تعيين عرض عمود النص بالنقاط. |

### ملاحظات

`TextColumn` يتم استخدام الكائنات فقط لتحديد الأعمدة ذات العرض والتباعد المخصصين. إذا كنت تريد أن تكون الأعمدة الموجودة في المستند متساوية العرض، فقم بتعيين TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) ل`حقيقي`.

عندما جديد`TextColumn` تم إنشاؤه وتم ضبط عرضه وتباعده على الصفر.

### أمثلة

يوضح كيفية إنشاء أعمدة متباعدة بشكل غير متساو.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// حدد مقدار المساحة المتوفرة لدينا لترتيب الأعمدة.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// قم بتعيين العمود الأول ليكون ضيقًا.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// اضبط العمود الثاني ليأخذ باقي المساحة المتوفرة في هوامش الصفحة.
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


