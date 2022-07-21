---
title: Row
second_title: Aspose.Words لمراجع .NET API
description: يمثل صف جدول .
type: docs
weight: 6010
url: /ar/net/aspose.words.tables/row/
---
## Row class

يمثل صف جدول .

```csharp
public class Row : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Row](row)(DocumentBase) | يقوم بتهيئة مثيل جديد لملف **صف** فئة . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Cells](../../aspose.words.tables/row/cells) { get; } | يوفر وصولاً مكتوبًا إلى ملف **خلية** العقد الفرعية للصف . |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص . |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [FirstCell](../../aspose.words.tables/row/firstcell) { get; } | إرجاع أول **خلية** في الصف . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | الحصول على الطفل الأول للعقدة . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsFirstRow](../../aspose.words.tables/row/isfirstrow) { get; } | صواب إذا كان هذا هو الصف الأول في الجدول ؛ خطأ بخلاف ذلك. |
| [IsLastRow](../../aspose.words.tables/row/islastrow) { get; } | صواب إذا كان هذا هو الصف الأخير في الجدول ؛ خطأ بخلاف ذلك. |
| [LastCell](../../aspose.words.tables/row/lastcell) { get; } | إرجاع الأخير **خلية** في الصف . |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | الحصول على آخر تابع للعقدة . |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.tables/row/nodetype) { get; } | عوائد **NodeType.Row** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentTable](../../aspose.words.tables/row/parenttable) { get; } | إرجاع الجدول الأصل المباشر للصف. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [RowFormat](../../aspose.words.tables/row/rowformat) { get; } | يوفر الوصول إلى خصائص تنسيق الصف. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.tables/row/accept)(DocumentVisitor) | يقبل الزائر . |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/row/ensureminimum)() | إذا كان ملف **صف** لا يحتوي على خلايا ، يقوم بإنشاء وإلحاق خلية واحدة **خلية** . |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة . |
| override [GetText](../../aspose.words.tables/row/gettext)() | الحصول على نص جميع الخلايا في هذا الصف بما في ذلك نهاية حرف الصف. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة . |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | يزيل كافة العقد التابعة للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag) العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

**صف** يمكن أن يكون فقط طفلًا من **الطاولة**.

**صف** يمكن أن تحتوي على واحد أو أكثر **خلية** العقد.

الحد الأدنى من الصف الصالح يحتاج إلى واحد على الأقل **خلية**.

### أمثلة

يوضح كيفية إنشاء جدول.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// تحتوي الجداول على صفوف تحتوي على خلايا قد تحتوي على فقرات
// مع عناصر نموذجية مثل المسارات والأشكال وحتى الجداول الأخرى.
// استدعاء طريقة "ضمان الحد الأدنى" على الطاولة سيضمن ذلك
// يحتوي الجدول على صف وخلية وفقرة واحدة على الأقل.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// أضف نصًا إلى المكالمة الأولى في الصف الأول من الجدول.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

يوضح كيفية التكرار عبر جميع الجداول في المستند وطباعة محتويات كل خلية.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // يمكننا استخدام طريقة "ToArray" في مجموعة صف لاستنساخها في مصفوفة.
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

يوضح كيفية إنشاء جدول متداخل بدون استخدام منشئ المستندات.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // أنشئ الجدول الخارجي بثلاثة صفوف وأربعة أعمدة ، ثم أضفه إلى المستند.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // أنشئ جدولًا آخر يحتوي على صفين وعمودين ثم أدخله في الخلية الأولى في الجدول الأول.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// ينشئ جدولًا جديدًا في المستند بالأبعاد المحددة والنص في كل خلية.
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

    // يمكنك استخدام خصائص "العنوان" و "الوصف" لإضافة عنوان ووصف على التوالي إلى جدولك.
    // يجب أن يحتوي الجدول على صف واحد على الأقل قبل أن نتمكن من استخدام هذه الخصائص.
    // هذه الخصائص مفيدة لمستندات .docx المتوافقة مع ISO / IEC 29500 (انظر فئة OoxmlCompliance).
    // إذا قمنا بحفظ المستند بتنسيقات ما قبل ISO / IEC 29500 ، فإن Microsoft Word يتجاهل هذه الخصائص.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### أنظر أيضا

* class [CompositeNode](../../aspose.words/compositenode)
* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
