---
title: NodeType Enum
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.NodeType للتعرف بسهولة على أنواع مختلفة من عقد مستندات Word وإدارتها لمعالجة المستندات بسلاسة.
type: docs
weight: 4920
url: /ar/net/aspose.words/nodetype/
---
## NodeType enumeration

يحدد نوع عقدة مستند Word.

```csharp
public enum NodeType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Any | `0` | يشير إلى جميع أنواع العقد. يسمح باختيار جميع العناصر الفرعية. |
| Document | `1` | أ[`Document`](../document/) الكائن الذي، باعتباره جذر شجرة المستندات، يوفر الوصول إلى مستند Word بأكمله. |
| Section | `2` | أ[`Section`](../section/) كائن يتوافق مع قسم واحد في مستند Word. |
| Body | `3` | أ[`Body`](../body/) كائن يحتوي على النص الرئيسي لقسم (قصة النص الرئيسي). |
| HeaderFooter | `4` | أ[`HeaderFooter`](../headerfooter/) كائن يحتوي على نص رأس أو تذييل معين داخل قسم. |
| Table | `5` | أ[`Table`](../../aspose.words.tables/table/) كائن يمثل جدولاً في مستند Word. |
| Row | `6` | صف من الجدول. |
| Cell | `7` | خلية من صف الجدول. |
| Paragraph | `8` | فقرة من النص. |
| BookmarkStart | `9` | بداية علامة مرجعية. |
| BookmarkEnd | `10` | نهاية علامة مرجعية. |
| EditableRangeStart | `11` | بداية نطاق قابل للتحرير. |
| EditableRangeEnd | `12` | نهاية نطاق قابل للتحرير. |
| MoveFromRangeStart | `13` | بداية نطاق MoveFrom. |
| MoveFromRangeEnd | `14` | نهاية نطاق MoveFrom. |
| MoveToRangeStart | `15` | بداية لمجموعة MoveTo. |
| MoveToRangeEnd | `16` | نهاية نطاق MoveTo. |
| GroupShape | `17` | مجموعة من الأشكال أو الصور أو كائنات OLE أو أشكال المجموعة الأخرى. |
| Shape | `18` | كائن رسم، مثل شكل OfficeArt أو صورة أو كائن OLE. |
| Comment | `19` | تعليق في مستند Word. |
| Footnote | `20` | حاشية سفلية أو ملاحظة ختامية في مستند Word. |
| Run | `21` | سلسلة من النصوص. |
| FieldStart | `22` | حرف خاص يشير إلى بداية حقل Word. |
| FieldSeparator | `23` | حرف خاص يفصل رمز الحقل عن نتيجة الحقل. |
| FieldEnd | `24` | حرف خاص يشير إلى نهاية حقل Word. |
| FormField | `25` | حقل النموذج. |
| SpecialChar | `26` | حرف خاص ليس من بين أنواع الأحرف الخاصة الأكثر تحديدًا. |
| SmartTag | `27` | علامة ذكية حول بنية مضمنة واحدة أو أكثر (تشغيلات، صور، حقول، إلخ.) ضمن فقرة |
| StructuredDocumentTag | `28` | يسمح بتحديد المعلومات الخاصة بالعملاء ووسائل تقديمها. |
| StructuredDocumentTagRangeStart | `29` | بداية**متباعد** علامة مستند منظمة تقبل محتوى متعدد الأقسام. |
| StructuredDocumentTagRangeEnd | `30` | نهاية**متباعد** علامة مستند منظمة تقبل محتوى متعدد الأقسام. |
| GlossaryDocument | `31` | وثيقة المصطلحات ضمن الوثيقة الرئيسية. |
| BuildingBlock | `32` | كتلة بناء داخل مستند المصطلحات (على سبيل المثال إدخال مستند المصطلحات). |
| CommentRangeStart | `33` | عقدة علامة تمثل بداية نطاق معلق. |
| CommentRangeEnd | `34` | عقدة علامة تمثل نهاية النطاق المعلق. |
| OfficeMath | `35` | كائن رياضيات مكتبي. يمكن أن يكون معادلة، أو دالة، أو مصفوفة، أو أي كائن رياضي آخر. يمكن أن يكون مجموعة من الكائنات الرياضية، ويمكن أن يحتوي أيضًا على كائنات غير رياضية، مثل سلاسل النصوص. |
| SubDocument | `36` | عقدة مستند فرعي وهي عبارة عن رابط إلى مستند آخر. |
| System | `37` | محجوز للاستخدام الداخلي بواسطة Aspose.Words. |
| Null | `38` | محجوز للاستخدام الداخلي بواسطة Aspose.Words. |

## أمثلة

يوضح كيفية التنقل عبر مجموعة العقد الفرعية للعقدة المركبة.

```csharp
Document doc = new Document();

// أضف تشغيلتين وشكلًا واحدًا كعقد فرعية إلى الفقرة الأولى من هذه الوثيقة.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// لاحظ أن 'CustomNodeId' لا يتم حفظه في ملف إخراج ولا يوجد إلا أثناء عمر العقدة.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// قم بالتكرار خلال مجموعة الأطفال المباشرين للفقرة،
// وطباعة أي مسارات أو أشكال نجدها بالداخل.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

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
            break;
    }
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
