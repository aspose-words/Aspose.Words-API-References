---
title: StoryType Enum
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.StoryType enum، وأدر نصوص مستندات Word بكفاءة وسهولة. حسّن تجربة معالجة مستنداتك اليوم!
type: docs
weight: 6970
url: /ar/net/aspose.words/storytype/
---
## StoryType enumeration

يتم تخزين نص مستند Word في القصص.`StoryType` يحدد قصة.

```csharp
public enum StoryType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | القيمة الافتراضية. لا توجد قصة مماثلة في المستند. |
| MainText | `1` | يحتوي على النص الرئيسي للمستند، والذي يمثله[`Body`](../body/) . |
| Footnotes | `2` | يحتوي على نص الحاشية السفلية، ويمثله[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | يحتوي على نص الحواشي الختامية، ويمثله[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | يحتوي على تعليقات المستند (الحواشي التوضيحية)، والتي يتم تمثيلها بواسطة[`Comment`](../comment/) . |
| Textbox | `5` | يحتوي على شكل أو نص مربع نص، يتم تمثيله بواسطة[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | يحتوي على نص رأس الصفحات الزوجية، والذي يمثله[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | يحتوي على نص رأس الصفحة الرئيسي. عندما يختلف رأس الصفحة للصفحات الفردية والزوجية، يحتوي على نص رأس الصفحة الفردية. يُمثل بـ[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | يحتوي على نص تذييل الصفحات الزوجية، والذي يمثله[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | يحتوي على نص التذييل الرئيسي. عندما يختلف التذييل للصفحات الفردية عن الزوجية، يحتوي على نص تذييل الصفحات الفردية. يُمثل بـ[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | يحتوي على نص رأس الصفحة الأولى، والذي يتم تمثيله بواسطة[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | يحتوي على نص تذييل الصفحة الأولى، والذي يتم تمثيله بواسطة[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | يحتوي على نص فاصل الحاشية السفلية. |
| FootnoteContinuationSeparator | `13` | يحتوي على نص فاصل استمرار الحاشية السفلية. |
| FootnoteContinuationNotice | `14` | يحتوي على نص فاصل إشعار استمرار الحاشية السفلية. |
| EndnoteSeparator | `15` | يحتوي على نص فاصل الحاشية الختامية. |
| EndnoteContinuationSeparator | `16` | يحتوي على نص فاصل استمرارية الحاشية. |
| EndnoteContinuationNotice | `17` | يحتوي على نص فاصل إشعار استمرار الحاشية الختامية. |

## أمثلة

يوضح كيفية إزالة كافة الأشكال من العقدة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم DocumentBuilder لإدراج شكل. هذا شكل مضمّن،
// والتي تحتوي على فقرة رئيسية، وهي عقدة فرعية لجسم القسم الأول.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

//يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا النص.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
