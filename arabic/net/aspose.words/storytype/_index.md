---
title: Enum StoryType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.StoryType تعداد. يتم تخزين نص مستند Word في مجموعات نصية. نوع القصة يحدد قصة.
type: docs
weight: 5820
url: /ar/net/aspose.words/storytype/
---
## StoryType enumeration

يتم تخزين نص مستند Word في مجموعات نصية. **نوع القصة** يحدد قصة.

```csharp
public enum StoryType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | القيمة الافتراضية. لا توجد مثل هذه القصة في الوثيقة. |
| MainText | `1` | يحتوي على النص الرئيسي للمستند ، الذي يمثله[`Body`](../body/) . |
| Footnotes | `2` | يحتوي على نص حاشية سفلية ، يتم تمثيله بواسطة[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | يحتوي على نص تعليقات ختامية ، يتم تمثيله بواسطة[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | يحتوي على تعليقات المستند (التعليقات التوضيحية) ، التي يمثلها[`Comment`](../comment/) . |
| Textbox | `5` | يحتوي على شكل أو نص مربع نص ، يتم تمثيله بواسطة[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | يحتوي على نص رأس الصفحات الزوجية ، ويمثله[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | يحتوي على نص الرأس الأساسي. عندما يكون العنوان مختلفًا للصفحات الفردية والزوجية ، يحتوي على نص رأس الصفحات الفردية. يتمثل ب[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | يحتوي على نص تذييل الصفحات الزوجية ، الذي يمثله[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | يحتوي على نص التذييل الأساسي. عندما يكون التذييل مختلفًا للصفحات الفردية والزوجية ، يحتوي على نص تذييل الصفحات الفردية. يتمثل ب[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | يحتوي على نص رأس الصفحة الأولى ، ويمثله[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | يحتوي على نص تذييل الصفحة الأولى ، ويمثله[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | يحتوي على نص فاصل الحواشي السفلية ، الذي يمثلهFootnoteSeparator . |
| FootnoteContinuationSeparator | `13` | يحتوي على نص فاصل متابعة الحواشي السفلية ، الذي يمثلهFootnoteSeparator . |
| FootnoteContinuationNotice | `14` | يحتوي على نص فاصل إشعار متابعة الحاشية السفلية ، الذي يمثلهFootnoteSeparator . |
| EndnoteSeparator | `15` | يحتوي على نص فاصل التعليقات الختامية ، الذي يمثلهFootnoteSeparator . |
| EndnoteContinuationSeparator | `16` | يحتوي على نص فاصل متابعة التعليقات الختامية ، الذي يمثلهFootnoteSeparator . |
| EndnoteContinuationNotice | `17` | يحتوي على نص فاصل إشعار متابعة التعليقات الختامية ، الذي يمثلهFootnoteSeparator . |

### أمثلة

يوضح كيفية إزالة كافة الأشكال من العقدة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم DocumentBuilder لإدراج شكل. هذا شكل مضمّن ،
// التي تحتوي على فقرة أصل ، وهي عقدة فرعية لنص القسم الأول.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا النص.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


