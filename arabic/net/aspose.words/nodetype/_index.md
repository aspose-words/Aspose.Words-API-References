---
title: Enum NodeType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.NodeType تعداد. يحدد نوع عقدة مستند Word .
type: docs
weight: 3990
url: /ar/net/aspose.words/nodetype/
---
## NodeType enumeration

يحدد نوع عقدة مستند Word .

```csharp
public enum NodeType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Any | `0` | يشير إلى كافة أنواع العقد. يسمح بتحديد جميع الأطفال. |
| Document | `1` | أ[`Document`](../document/) الكائن الذي ، باعتباره جذر شجرة المستند ، يوفر الوصول إلى مستند Word بأكمله. |
| Section | `2` | أ[`Section`](../section/) الكائن الذي يتوافق مع قسم واحد في مستند Word. |
| Body | `3` | أ[`Body`](../body/) الكائن الذي يحتوي على النص الرئيسي للقسم (قصة النص الرئيسي). |
| HeaderFooter | `4` | أ[`HeaderFooter`](../headerfooter/) كائن يحتوي على نص رأس أو تذييل معين داخل قسم. |
| Table | `5` | أ[`Table`](../../aspose.words.tables/table/) يمثل جدولاً في مستند Word. |
| Row | `6` | صف من الجدول. |
| Cell | `7` | خلية صف جدول. |
| Paragraph | `8` | فقرة من النص. |
| BookmarkStart | `9` | بداية علامة الإشارة المرجعية. |
| BookmarkEnd | `10` | نهاية علامة الإشارة المرجعية. |
| EditableRangeStart | `11` | بداية نطاق قابل للتحرير. |
| EditableRangeEnd | `12` | نهاية نطاق قابل للتحرير. |
| MoveFromRangeStart | `13` | بداية نطاق MoveFrom. |
| MoveFromRangeEnd | `14` | نهاية نطاق MoveFrom. |
| MoveToRangeStart | `15` | بداية نطاق MoveTo. |
| MoveToRangeEnd | `16` | نهاية نطاق MoveTo. |
| GroupShape | `17` | مجموعة من الأشكال أو الصور أو كائنات OLE أو أشكال المجموعة الأخرى. |
| Shape | `18` | عنصر رسومي ، مثل شكل OfficeArt أو صوره أو عنصر OLE. |
| Comment | `19` | تعليق في مستند Word. |
| Footnote | `20` | حاشية سفلية أو تعليق ختامي في مستند Word. |
| Run | `21` | سلسلة نصية. |
| FieldStart | `22` | حرف خاص يحدد بداية حقل Word. |
| FieldSeparator | `23` | حرف خاص يفصل رمز الحقل عن نتيجة الحقل. |
| FieldEnd | `24` | حرف خاص يحدد نهاية حقل Word. |
| FormField | `25` | حقل نموذج. |
| SpecialChar | `26` | حرف خاص ليس من أنواع الأحرف الخاصة الأكثر تحديدًا. |
| SmartTag | `27` | علامة ذكية حول واحد أو أكثر من الهياكل المضمنة (عمليات التشغيل ، الصور ، الحقول ، إلخ) داخل فقرة |
| StructuredDocumentTag | `28` | يسمح بتحديد المعلومات الخاصة بالعميل ووسائل عرضها. |
| StructuredDocumentTagRangeStart | `29` | بداية **تراوحت** علامة المستند المهيكلة التي تقبل المحتوى متعدد الأقسام. |
| StructuredDocumentTagRangeEnd | `30` | نهاية **تراوحت** علامة المستند المهيكلة التي تقبل المحتوى متعدد الأقسام. |
| GlossaryDocument | `31` | وثيقة مسرد داخل الوثيقة الرئيسية. |
| BuildingBlock | `32` | عنصر أساسي داخل مستند مسرد (على سبيل المثال إدخال مستند مسرد). |
| CommentRangeStart | `33` | عقدة علامة تمثل بداية نطاق معلق. |
| CommentRangeEnd | `34` | عقدة علامة تمثل نهاية نطاق معلق. |
| OfficeMath | `35` | كائن Office Math. يمكن أن تكون معادلة أو دالة أو مصفوفة أو أحد الكائنات الرياضية الأخرى. يمكن أن تكون مجموعة من العناصر الرياضية ويمكن أن تحتوي أيضًا على بعض الكائنات غير الرياضية مثل عمليات تشغيل النص. |
| SubDocument | `36` | عقدة مستند ثانوي وهي ارتباط إلى مستند آخر. |
| System | `37` | محجوزة للاستخدام الداخلي بواسطة Aspose.Words. |
| Null | `38` | محجوزة للاستخدام الداخلي بواسطة Aspose.Words. |

### أمثلة

يوضح كيفية اجتياز مجموعة العقد المركبة الخاصة بالعقد الفرعية.

```csharp
Document doc = new Document();

// أضف شريطين وشكل واحد كعقد فرعية إلى الفقرة الأولى من هذا المستند.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// لاحظ أن "CustomNodeId" لا يتم حفظه في ملف الإخراج ولا يوجد إلا أثناء عمر العقدة.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// كرر من خلال مجموعة الفقرة للأطفال المباشرين ،
// وطباعة أي أشكال أو أشكال نجدها بالداخل.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
    }
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


