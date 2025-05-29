---
title: Row Class
linktitle: Row
articleTitle: Row
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Tables.Row لإدارة صفوف الجداول بسلاسة في مستنداتك. حسّن معالجة مستنداتك بميزات فعّالة!
type: docs
weight: 7160
url: /ar/net/aspose.words.tables/row/
---
## Row class

يمثل صف الجدول.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public class Row : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Row](row/)(*[DocumentBase](../../aspose.words/documentbase/)*) | يقوم بتهيئة مثيل جديد لـ`Row` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Cells](../../aspose.words.tables/row/cells/) { get; } | يوفر الوصول المكتوب إلى[`Cell`](../cell/) العقد الفرعية للصف. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstCell](../../aspose.words.tables/row/firstcell/) { get; } | يعيد أول[`Cell`](../cell/) في الصف. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [IsFirstRow](../../aspose.words.tables/row/isfirstrow/) { get; } | صحيح إذا كان هذا هو الصف الأول في الجدول؛ وإلا فهو خطأ. |
| [IsLastRow](../../aspose.words.tables/row/islastrow/) { get; } | صحيح إذا كان هذا هو الصف الأخير في الجدول؛ وإلا يكون خطأ. |
| [LastCell](../../aspose.words.tables/row/lastcell/) { get; } | يعيد آخر[`Cell`](../cell/) في الصف. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [NextRow](../../aspose.words.tables/row/nextrow/) { get; } | يحصل على التالي`Row` العقدة. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.tables/row/nodetype/) { get; } | إرجاعRow . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentTable](../../aspose.words.tables/row/parenttable/) { get; } | يعيد الجدول الرئيسي المباشر للصف. |
| [PreviousRow](../../aspose.words.tables/row/previousrow/) { get; } | يحصل على السابق`Row` العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [RowFormat](../../aspose.words.tables/row/rowformat/) { get; } | يوفر الوصول إلى خصائص التنسيق الخاصة بالصف. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.tables/row/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words.tables/row/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة نهاية الصف. |
| override [AcceptStart](../../aspose.words.tables/row/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة بداية الصف. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [EnsureMinimum](../../aspose.words.tables/row/ensureminimum/)() | إذا كان`Row` لا يحتوي على خلايا، بل ينشئ ويضيف واحدة[`Cell`](../cell/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | يعيد عقدة فرعية رقم N تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words.tables/row/gettext/)() | يحصل على نص جميع الخلايا في هذا الصف بما في ذلك حرف نهاية الصف. |
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
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

`Row` لا يمكن أن يكون إلا طفلاً لـ[`Table`](../table/).

`Row` يمكن أن تحتوي على واحد أو أكثر[`Cell`](../cell/) العقد.

يجب أن يحتوي الصف الصحيح الأدنى على صف واحد على الأقل[`Cell`](../cell/).

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
