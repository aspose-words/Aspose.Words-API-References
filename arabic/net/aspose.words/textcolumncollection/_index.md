---
title: TextColumnCollection Class
linktitle: TextColumnCollection
articleTitle: TextColumnCollection
second_title: Aspose.Words لـ .NET
description: استكشف Aspose.Words.TextColumnCollection لإدارة أعمدة النص في مستنداتك بسهولة. حسّن تنسيق مستنداتك بسهولة!
type: docs
weight: 7250
url: /ar/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

مجموعة من[`TextColumn`](../textcolumn/) الكائنات التي تمثل جميع أعمدة النص في قسم من المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأقسام](https://docs.aspose.com/words/net/working-with-sections/) مقالة توثيقية.

```csharp
public class TextColumnCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | يحصل على عدد الأعمدة في قسم المستند. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | صحيح إذا كانت أعمدة النص متساوية العرض ومتباعدة بشكل متساوٍ. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | يعيد عمود نص عند الفهرس المحدد. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | عندما`حقيقي` ، يضيف خطًا رأسيًا بين الأعمدة. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | عندما تكون المسافة بين الأعمدة متساوية، يتم الحصول على مقدار المسافة بين كل عمود بالنقاط أو تعيينه. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | عندما تكون المسافة بين الأعمدة متساوية، يتم الحصول على عرض الأعمدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(*int*) | يقوم بترتيب النص في العدد المحدد من أعمدة النص. |

## ملاحظات

يستخدم[`SetCount`](./setcount/) لتعيين عدد أعمدة النص.

لجعل جميع الأعمدة متساوية العرض ومتباعدة بشكل متساوٍ، اضبط[`EvenlySpaced`](./evenlyspaced/) ل`حقيقي` وحدد مقدار المساحة بين الأعمدة في[`Spacing`](./spacing/)سيقوم MS Word بحساب عرض الأعمدة تلقائيًا.

إذا كان لديك[`EvenlySpaced`](./evenlyspaced/) تم ضبطه على`خطأ شنيع` يجب تحديد العرض والتباعد لكل عمود x000d_ على حدة. استخدم الفهرس للوصول إلى كل عمود على حدة.[`TextColumn`](../textcolumn/) أشياء.

عند استخدام عرض الأعمدة المخصص، تأكد من أن مجموع كل عرض الأعمدة والمسافات بينها يساوي عرض الصفحة مطروحًا منه الهوامش اليمنى واليسرى للصفحة.

## أمثلة

يوضح كيفية إنشاء عدة أعمدة متباعدة بشكل متساوٍ في قسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
