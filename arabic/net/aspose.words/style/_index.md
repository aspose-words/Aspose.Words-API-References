---
title: Style Class
linktitle: Style
articleTitle: Style
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Style فصل. يمثل نمطًا واحدًا مدمجًا أو محددًا من قبل المستخدم في C#.
type: docs
weight: 6130
url: /ar/net/aspose.words/style/
---
## Style class

يمثل نمطًا واحدًا مدمجًا أو محددًا من قبل المستخدم.

لمعرفة المزيد، قم بزيارة[العمل مع الأنماط والموضوعات](https://docs.aspose.com/words/net/working-with-styles-and-themes/) مقالة توثيقية.

```csharp
public class Style
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | يحصل على كافة الأسماء المستعارة لهذا النمط. إذا لم يكن النمط يحتوي على أسماء مستعارة، فسيتم إرجاع مجموعة فارغة من السلسلة. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | يحدد ما إذا كان سيتم إعادة تعريف هذا النمط تلقائيًا بناءً على القيمة المناسبة. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | الحصول على/تعيين اسم النمط الذي يعتمد عليه هذا النمط. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | صحيح إذا كان هذا النمط أحد الأنماط المضمنة في برنامج MS Word. |
| [Document](../../aspose.words/style/document/) { get; } | الحصول على مستند المالك. |
| [Font](../../aspose.words/style/font/) { get; } | الحصول على تنسيق الأحرف للنمط. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | صحيح عندما يكون النمط أحد أنماط العناوين المضمنة. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | يحدد ما إذا كان سيتم عرض هذا النمط في معرض "الأنماط السريعة" داخل واجهة مستخدم MS Word. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | يحصل على اسم`Style` مرتبطة بهذا. إرجاع سلسلة فارغة إذا لم يتم ربط أي أنماط. |
| [List](../../aspose.words/style/list/) { get; } | الحصول على القائمة التي تحدد تنسيق نمط القائمة هذا. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة. |
| [Name](../../aspose.words/style/name/) { get; set; } | الحصول على اسم النمط أو تعيينه. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | الحصول على/تعيين اسم النمط الذي سيتم تطبيقه تلقائيًا على فقرة جديدة تم إدراجها بعد a فقرة منسقة بالنمط المحدد. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | الحصول على تنسيق الفقرة للنمط. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | الحصول على معرف النمط المحلي المستقل للنمط المدمج. |
| [Styles](../../aspose.words/style/styles/) { get; } | الحصول على مجموعة الأنماط التي ينتمي إليها هذا النمط. |
| [Type](../../aspose.words/style/type/) { get; } | الحصول على نوع النمط (فقرة أو حرف). |

## طُرق

| اسم | وصف |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(*Style*) | يقارن مع النمط المحدد. تتم مقارنة أنماط الأنماط للأنماط المضمنة فقط. لا يتم تضمين افتراضيات الأنماط في المقارنة. تتم مقارنة النمط الأساسي والنمط المرتبط ونمط الفقرة التالية بشكل متكرر. |
| [Remove](../../aspose.words/style/remove/)() | إزالة النمط المحدد من المستند. |

## أمثلة

يوضح كيفية إنشاء نمط فقرة واستخدامه بتنسيق القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء نمط فقرة مخصص.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// أنشئ قائمة وتأكد من أن الفقرات التي تستخدم هذا النمط ستستخدم هذه القائمة.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// قم بتطبيق نمط الفقرة على الفقرة الحالية لمنشئ المستند، ثم قم بإضافة بعض النص.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// قم بتغيير نمط منشئ المستندات إلى نمط لا يحتوي على تنسيق قائمة واكتب فقرة أخرى.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

يوضح كيفية إنشاء نمط مخصص وتطبيقه.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// إعادة تعريف النمط تلقائيًا.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق أحد الأنماط من المستند على الفقرة التي يقوم منشئ المستند بإنشائها.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// قم بإزالة النمط المخصص لدينا من مجموعة أنماط المستند.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// أي نص يستخدم نمطًا تمت إزالته يعود إلى التنسيق الافتراضي.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
