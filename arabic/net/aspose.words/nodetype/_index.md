---
title: Enum NodeType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.NodeType تعداد. يحدد نوع عقدة مستند Word.
type: docs
weight: 4230
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
| Any | `0` | يشير إلى جميع أنواع العقد. يسمح بتحديد جميع الأطفال. |
| Document | `1` | أ[`Document`](../document/) كائن، باعتباره جذر شجرة المستندات، يوفر الوصول إلى مستند Word بأكمله. |
| Section | `2` | أ[`Section`](../section/) كائن يتوافق مع قسم واحد في مستند Word. |
| Body | `3` | أ[`Body`](../body/) كائن يحتوي على النص الرئيسي للقسم (قصة النص الرئيسي). |
| HeaderFooter | `4` | أ[`HeaderFooter`](../headerfooter/) كائن يحتوي على نص رأس أو تذييل معين داخل القسم. |
| Table | `5` | أ[`Table`](../../aspose.words.tables/table/) كائن يمثل جدولاً في مستند Word. |
| Row | `6` | صف من الجدول. |
| Cell | `7` | خلية صف الجدول. |
| Paragraph | `8` | فقرة من النص. |
| BookmarkStart | `9` | بداية علامة مرجعية. |
| BookmarkEnd | `10` | نهاية علامة مرجعية. |
| EditableRangeStart | `11` | بداية نطاق قابل للتحرير. |
| EditableRangeEnd | `12` | نهاية النطاق القابل للتحرير. |
| MoveFromRangeStart | `13` | بداية نطاق MoveFrom. |
| MoveFromRangeEnd | `14` | نهاية نطاق MoveFrom. |
| MoveToRangeStart | `15` | بداية نطاق MoveTo. |
| MoveToRangeEnd | `16` | نهاية نطاق MoveTo. |
| GroupShape | `17` | مجموعة من الأشكال أو الصور أو كائنات OLE أو أشكال المجموعة الأخرى. |
| Shape | `18` | كائن رسومي، مثل شكل OfficeArt أو صورة أو كائن OLE. |
| Comment | `19` | تعليق في مستند Word. |
| Footnote | `20` | حاشية سفلية أو تعليق ختامي في مستند Word. |
| Run | `21` | تشغيل النص. |
| FieldStart | `22` | حرف خاص يحدد بداية حقل Word. |
| FieldSeparator | `23` | حرف خاص يفصل رمز الحقل عن نتيجة الحقل. |
| FieldEnd | `24` | حرف خاص يحدد نهاية حقل Word. |
| FormField | `25` | حقل النموذج. |
| SpecialChar | `26` | حرف خاص لا يعد أحد أنواع الأحرف الخاصة الأكثر تحديدًا. |
| SmartTag | `27` | علامة ذكية حول بنية سطرية واحدة أو أكثر (عمليات التشغيل والصور والحقول وما إلى ذلك) داخل الفقرة |
| StructuredDocumentTag | `28` | يسمح بتحديد المعلومات الخاصة بالعميل ووسائل عرضها. |
| StructuredDocumentTagRangeStart | `29` | بداية **تراوحت** علامة مستند منظمة تقبل محتوى متعدد الأقسام. |
| StructuredDocumentTagRangeEnd | `30` | نهاية **تراوحت** علامة مستند منظمة تقبل محتوى متعدد الأقسام. |
| GlossaryDocument | `31` | مستند مسرد ضمن الوثيقة الرئيسية. |
| BuildingBlock | `32` | كتلة بناء داخل مستند المسرد (على سبيل المثال، إدخال مستند المسرد). |
| CommentRangeStart | `33` | عقدة علامة تمثل بداية النطاق الذي تم التعليق عليه. |
| CommentRangeEnd | `34` | عقدة علامة تمثل نهاية النطاق الذي تم التعليق عليه. |
| OfficeMath | `35` | كائن Office Math. يمكن أن تكون معادلة أو دالة أو مصفوفة أو أحد الكائنات الرياضية الأخرى. يمكن أن تكون مجموعة من الكائنات الرياضية ويمكن أن تحتوي أيضًا على بعض الكائنات غير الرياضية مثل مجموعة من النصوص. |
| SubDocument | `36` | عقدة مستند ثانوي وهي عبارة عن رابط لمستند آخر. |
| System | `37` | محجوز للاستخدام الداخلي بواسطة Aspose.Words. |
| Null | `38` | محجوز للاستخدام الداخلي بواسطة Aspose.Words. |

### أمثلة

يوضح كيفية اجتياز مجموعة العقد الفرعية للعقدة المركبة.

```csharp
Document doc = new Document();

// أضف مسارين وشكلًا واحدًا كعقد فرعية إلى الفقرة الأولى من هذه الوثيقة.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// لاحظ أن "CustomNodeId" لا يتم حفظه في ملف إخراج وهو موجود فقط أثناء عمر العقدة.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// كرر من خلال مجموعة الفقرة من العناصر الفرعية المباشرة،
// وطباعة أي مسارات أو أشكال نجدها داخلها.
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


