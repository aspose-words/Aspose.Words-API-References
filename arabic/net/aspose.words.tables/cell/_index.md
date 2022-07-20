---
title: Cell
second_title: Aspose.Words لمراجع .NET API
description: يمثل خلية جدول .
type: docs
weight: 5940
url: /ar/net/aspose.words.tables/cell/
---
## Cell class

يمثل خلية جدول .

```csharp
public class Cell : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Cell](cell)(DocumentBase) | يقوم بتهيئة مثيل جديد لملف **خلية** فئة ._ x000d_ |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CellFormat](../../aspose.words.tables/cell/cellformat) { get; } | يوفر الوصول إلى خصائص تنسيق الخلية. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص ._ x000d_ |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | الحصول على الطفل الأول للعقدة . |
| [FirstParagraph](../../aspose.words.tables/cell/firstparagraph) { get; } | يحصل على الفقرة الأولى بين الأطفال المباشرين. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsFirstCell](../../aspose.words.tables/cell/isfirstcell) { get; } | صحيح إذا كانت هذه هي الخلية الأولى داخل الصف ؛ خطأ بخلاف ذلك. |
| [IsLastCell](../../aspose.words.tables/cell/islastcell) { get; } | صحيح إذا كانت هذه هي الخلية الأخيرة داخل صف ؛ خطأ بخلاف ذلك. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | الحصول على آخر تابع للعقدة . |
| [LastParagraph](../../aspose.words.tables/cell/lastparagraph) { get; } | يحصل على الفقرة الأخيرة بين الأطفال المباشرين. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.tables/cell/nodetype) { get; } | عوائد **NodeType.Cell** . |
| [Paragraphs](../../aspose.words.tables/cell/paragraphs) { get; } | الحصول على مجموعة من الفقرات التي تعتبر توابع مباشرة للخلية. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentRow](../../aspose.words.tables/cell/parentrow) { get; } | إرجاع الصف الأصل للخلية. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [Tables](../../aspose.words.tables/cell/tables) { get; } | الحصول على مجموعة من الجداول التي هي توابع مباشرة للخلية. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.tables/cell/accept)(DocumentVisitor) | يقبل الزائر . |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/cell/ensureminimum)() | إذا لم يكن الطفل الأخير فقرة ، فسيتم إنشاء وإلحاق فقرة واحدة فارغة. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة ._ x000d_ |
| override [GetText](../../aspose.words/compositenode/gettext)() | يحصل على نص هذه العقدة وجميع توابعها. |
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

**خلية** يمكن أن يكون فقط طفلًا من **صف**.

**خلية** يمكن أن تحتوي على عقد على مستوى الكتلة **فقرة** و **الطاولة**.

الحد الأدنى من الخلية الصالحة يجب أن تحتوي على خلية واحدة على الأقل **فقرة**.

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
