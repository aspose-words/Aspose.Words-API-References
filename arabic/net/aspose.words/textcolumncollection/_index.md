---
title: Class TextColumnCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.TextColumnCollection فصل. مجموعة منTextColumn الكائنات التي تمثل كافة أعمدة النص في قسم من المستند.
type: docs
weight: 6400
url: /ar/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

مجموعة من[`TextColumn`](../textcolumn/) الكائنات التي تمثل كافة أعمدة النص في قسم من المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأقسام](https://docs.aspose.com/words/net/working-with-sections/) مقالة توثيقية.

```csharp
public class TextColumnCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | الحصول على عدد الأعمدة في قسم المستند. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | صحيح إذا كانت أعمدة النص متساوية العرض ومتباعدة بشكل متساوٍ. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | إرجاع عمود نصي في الفهرس المحدد. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | متى`حقيقي`يضيف خطًا رأسيًا بين الأعمدة. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | عندما تكون الأعمدة متباعدة بالتساوي، يتم الحصول على مقدار المسافة بين كل عمود أو تعيينه بالنقاط. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | عندما تكون الأعمدة متباعدة بشكل متساو، يتم الحصول على عرض الأعمدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(int) | ترتيب النص في العدد المحدد من أعمدة النص. |

### ملاحظات

يستخدم[`SetCount`](./setcount/) لتعيين عدد أعمدة النص.

لجعل جميع الأعمدة متساوية في العرض ومتباعدة بشكل متساوٍ، قم بتعيينها[`EvenlySpaced`](./evenlyspaced/) ل`حقيقي` وحدد مقدار المسافة بين الأعمدة الموجودة[`Spacing`](./spacing/). سوف يقوم برنامج MS Word بحساب عرض الأعمدة تلقائيًا.

اذا كنت تمتلك[`EvenlySpaced`](./evenlyspaced/) ضبط ل`خطأ شنيع` ، فأنت بحاجة إلى تحديد العرض والتباعد لكل عمود بشكل فردي. استخدم المفهرس للوصول إلى الفرد[`TextColumn`](../textcolumn/) أشياء.

عند استخدام عروض الأعمدة المخصصة، تأكد من أن مجموع كل عروض الأعمدة والمسافات بينها يساوي عرض الصفحة ناقص هوامش الصفحة اليمنى واليسرى.

### أمثلة

يوضح كيفية إنشاء عدة أعمدة متباعدة بشكل متساوٍ في القسم.

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


