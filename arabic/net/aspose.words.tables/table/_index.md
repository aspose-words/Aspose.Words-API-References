---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Tables.Table لإنشاء الجداول وإدارتها بسهولة في مستندات Word، مما يعزز تخطيط مستندك ووظائفه.
type: docs
weight: 7190
url: /ar/net/aspose.words.tables/table/
---
## Table class

يمثل جدولًا في مستند Word.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public class Table : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Table](table/)(*[DocumentBase](../../aspose.words/documentbase/)*) | يقوم بتهيئة مثيل جديد لـ`Table` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | يحصل على أو يعين موضع الجدول العائم الأفقي المطلق المحدد بواسطة خصائص الجدول، بالنقاط. القيمة الافتراضية هي 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | يحصل على أو يعين موضع الجدول العائم العمودي المطلق المحدد بواسطة خصائص الجدول، بالنقاط. القيمة الافتراضية هي 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | يحدد كيفية محاذاة جدول مضمن في المستند. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | يسمح لبرنامج Microsoft Word وAspose.Words بتغيير حجم الخلايا في الجدول تلقائيًا لتناسب محتوياتها. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | يحصل على خيار "السماح بالتباعد بين الخلايا" أو يعينه. |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | يحصل على ما إذا كان الجدول العائم يسمح للأشياء العائمة الأخرى في المستند بالتداخل مع امتداداته عند عرضها. القيمة الافتراضية هي`حقيقي` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | يحصل على أو يحدد ما إذا كان هذا جدولًا من اليمين إلى اليسار. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | يحصل على مقدار المساحة (بالنقاط) المراد إضافتها أسفل محتويات الخلايا أو يعينه. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | يحصل على مقدار المساحة (بالنقاط) بين الخلايا أو يعينها. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | يحصل على وصف هذا الجدول أو يعينه. يوفر تمثيلًا نصيًا بديلاً للمعلومات الموجودة في الجدول. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | يحصل على المسافة بين أسفل الجدول والنص المحيط بها، بالنقاط، أو يعينها. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | يحصل على أو يعين المسافة بين يسار الجدول والنص المحيط به، بالنقاط. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | يحصل على أو يعين المسافة بين يمين الجدول والنص المحيط به، بالنقاط. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | يحصل على المسافة بين أعلى الجدول والنص المحيط به، بالنقاط، أو يعينها. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | يعيد أول[`Row`](../row/) عقدة في الجدول. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | يحصل على الكائن الأساسي الذي يجب أن يتم حساب الموضع الأفقي للجدول العائم منه. القيمة الافتراضية هيColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | يعيد آخر[`Row`](../row/) عقدة في الجدول. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | يحصل على القيمة التي تمثل المسافة البادئة اليسرى للجدول أو يعينها. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | يحصل على مقدار المساحة (بالنقاط) التي يجب إضافتها إلى يسار محتويات الخلايا أو يعينها. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | إرجاعTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | يحصل على العرض المفضل للجدول أو يعينه. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | يحصل على محاذاة الجدول العائم الأفقية النسبية أو يعينها. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | يحصل على محاذاة الجدول العائم الرأسية النسبية أو يعينها. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | يحصل على مقدار المساحة (بالنقاط) التي يجب إضافتها إلى يمين محتويات الخلايا أو يعينها. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | يوفر الوصول المكتوب إلى صفوف الجدول. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | يحصل على نمط الجدول المطبق على هذا الجدول أو يعينه. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | يحصل على أو يعين معرف النمط المستقل عن الإعدادات المحلية لنمط الجدول المطبق على هذا الجدول. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | يحصل على اسم نمط الجدول المطبق على هذا الجدول أو يعينه. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | يحصل على أو يعين علامات البت التي تحدد كيفية تطبيق نمط الجدول على هذا الجدول. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | يحصل أو يعين[`TextWrapping`](./textwrapping/) للجدول. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | يحصل على عنوان هذا الجدول أو يعينه. يوفر تمثيلًا نصيًا بديلاً للمعلومات الموجودة في الجدول. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | يحصل على مقدار المساحة (بالنقاط) المراد إضافتها فوق محتويات الخلايا أو يعينه. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | يحصل على الكائن الأساسي الذي يجب أن يتم حساب الموضع الرأسي للجدول العائم منه. القيمة الافتراضية هيMargin . |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words.tables/table/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة نهاية الجدول. |
| override [AcceptStart](../../aspose.words.tables/table/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة بداية الجدول. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | تغيير حجم الجدول والخلايا وفقًا لسلوك الملاءمة التلقائية المحدد. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | يزيل جميع حدود الجدول والخلايا في هذا الجدول. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | يزيل كل التظليل على الجدول. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | يحول الخلايا المندمجة أفقيًا حسب العرض إلى خلايا مندمجة حسب[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | إذا لم يكن للجدول صفوف، يتم إنشاء صف وإضافته[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | يعيد عقدة فرعية رقم N تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | يعيد مؤشر العقدة الفرعية المحددة في مجموعة العقد الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة فورًا بعد عقدة المرجع المحددة. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل عقدة المرجع المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | يزيل العقدة الفرعية المحددة. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد المنحدرة من العقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | يحدد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | يحدد الأول[`Node`](../../aspose.words/node/) الذي يتطابق مع تعبير XPath. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | تعيين حدود الجدول المحددة إلى نمط الخط والعرض واللون المحددين. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | تعيين حدود جميع الجدول إلى نمط الخط والعرض واللون المحدد. |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | تعيين التظليل إلى القيم المحددة على الجدول بأكمله. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

`Table` هي عقدة على مستوى الكتلة ويمكن أن تكون طفلة للفئات المشتقة من[`Story`](../../aspose.words/story/) أو [`InlineStory`](../../aspose.words/inlinestory/).

`Table` يمكن أن تحتوي على واحد أو أكثر[`Row`](../row/) العقد.

يجب أن يحتوي الجدول الصحيح الأدنى على واحد على الأقل[`Row`](../row/).

## أمثلة

يوضح كيفية إنشاء جدول.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// تحتوي الجداول على صفوف تحتوي على خلايا، والتي قد تحتوي على فقرات
// مع العناصر النموذجية مثل التشغيلات والأشكال وحتى الجداول الأخرى.
// سيؤدي استدعاء طريقة "EnsureMinimum" على جدول إلى ضمان ذلك
//يحتوي الجدول على صف واحد وخلية وفقرة واحدة على الأقل.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

//أضف نصًا إلى الخلية الأولى في الصف الأول من الجدول.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

يوضح كيفية تكرار جميع الجداول في المستند وطباعة محتويات كل خلية.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // يمكننا استخدام طريقة "ToArray" على مجموعة صفوف لاستنساخها في مصفوفة.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // يمكننا استخدام طريقة "ToArray" على مجموعة خلايا لاستنساخها في مصفوفة.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

يوضح كيفية إنشاء جدول 2x2 منسق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// أثناء إنشاء الجدول، سيقوم منشئ المستند بتطبيق قيم خصائص RowFormat/CellFormat الحالية
// إلى الصف/الخلية الحالية التي يتواجد بها المؤشر وأي صفوف/خلايا جديدة أثناء إنشائها.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// لا تتأثر الصفوف والخلايا المضافة مسبقًا بأثر رجعي بالتغييرات التي تطرأ على تنسيق المنشئ.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

يوضح كيفية إنشاء جدول متداخل دون استخدام منشئ المستندات.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // قم بإنشاء الجدول الخارجي بثلاثة صفوف وأربعة أعمدة، ثم قم بإضافته إلى المستند.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // قم بإنشاء جدول آخر يحتوي على صفين وعمودين ثم أدخله في الخلية الأولى للجدول الأول.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// إنشاء جدول جديد في المستند بالأبعاد والنص المحددين في كل خلية.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    //يمكنك استخدام خصائص "العنوان" و"الوصف" لإضافة عنوان ووصف على التوالي إلى الجدول الخاص بك.
    // يجب أن يحتوي الجدول على صف واحد على الأقل قبل أن نتمكن من استخدام هذه الخصائص.
    // هذه الخصائص مفيدة للمستندات .docx المتوافقة مع ISO / IEC 29500 (انظر فئة OoxmlCompliance).
    // إذا قمنا بحفظ المستند بتنسيقات ما قبل ISO/IEC 29500، فإن Microsoft Word يتجاهل هذه الخصائص.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### أنظر أيضا

* class [CompositeNode](../../aspose.words/compositenode/)
* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
