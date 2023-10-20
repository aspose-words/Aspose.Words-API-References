---
title: StoryType Enum
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.StoryType تعداد. يتم تخزين نص مستند Word في القصص.StoryType يحدد القصة في C#.
type: docs
weight: 6120
url: /ar/net/aspose.words/storytype/
---
## StoryType enumeration

يتم تخزين نص مستند Word في القصص.`StoryType` يحدد القصة.

```csharp
public enum StoryType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | القيمة الافتراضية. لا يوجد مثل هذه القصة في الوثيقة. |
| MainText | `1` | يحتوي على النص الرئيسي للوثيقة، ممثلة بـ[`Body`](../body/) . |
| Footnotes | `2` | يحتوي على نص الحاشية السفلية، ممثلة بـ[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | يحتوي على نص الحواشي الختامية، ممثلة بـ[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | يحتوي على تعليقات الوثيقة (الشروح)، ممثلة بـ[`Comment`](../comment/) . |
| Textbox | `5` | يحتوي على شكل أو نص مربع نص، يمثله[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | يحتوي على نص رأس الصفحات الزوجية، ممثلة بـ[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | يحتوي على نص الرأس الأساسي. عندما يختلف الرأس بين الصفحات الفردية والزوجية، فإن يحتوي على نص رأس الصفحات الفردية. يتمثل ب[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | يحتوي على نص تذييل الصفحات الزوجية، ممثلة بـ[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | يحتوي على نص التذييل الأساسي. عندما يختلف التذييل بالنسبة للصفحات الفردية والزوجية، فإن يحتوي على نص تذييل الصفحات الفردية. يتمثل ب[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | يحتوي على نص رأس الصفحة الأولى، ممثلة بـ[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | يحتوي على نص تذييل الصفحة الأولى، ممثلة بـ[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | يحتوي على نص فاصل الحواشي السفلية، ممثلاً بـFootnoteSeparator . |
| FootnoteContinuationSeparator | `13` | يحتوي على نص فاصل متابعة الحاشية السفلية، ممثلاً بـFootnoteSeparator . |
| FootnoteContinuationNotice | `14` | يحتوي على نص فاصل إشعار استمرار الحاشية السفلية، ممثلاً بـFootnoteSeparator . |
| EndnoteSeparator | `15` | يحتوي على نص فاصل التعليقات الختامية، ممثلاً بـFootnoteSeparator . |
| EndnoteContinuationSeparator | `16` | يحتوي على نص فاصل استمرار التعليق الختامي، ممثلاً بـFootnoteSeparator . |
| EndnoteContinuationNotice | `17` | يحتوي على نص فاصل إشعار متابعة التعليق الختامي، ممثلاً بـFootnoteSeparator . |

## أمثلة

يوضح كيفية إزالة كافة الأشكال من العقدة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم DocumentBuilder لإدراج شكل. وهذا شكل خطي
// التي تحتوي على فقرة أصل، وهي عقدة فرعية لنص القسم الأول.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا الجسم.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
