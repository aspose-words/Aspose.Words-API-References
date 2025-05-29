---
title: Style Class
linktitle: Style
articleTitle: Style
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Style لإدارة الأنماط المخصصة والمضمنة بسهولة. حسّن تنسيق مستنداتك بسهولة ودقة.
type: docs
weight: 6980
url: /ar/net/aspose.words/style/
---
## Style class

يمثل نمطًا واحدًا مدمجًا أو محددًا بواسطة المستخدم.

لمعرفة المزيد، قم بزيارة[العمل مع الأنماط والموضوعات](https://docs.aspose.com/words/net/working-with-styles-and-themes/) مقالة توثيقية.

```csharp
public class Style
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | يحصل على جميع الأسماء المستعارة لهذا النمط. إذا لم يكن للنمط أسماء مستعارة، فسيتم إرجاع مصفوفة فارغة من السلسلة. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | يحدد ما إذا كان سيتم إعادة تعريف هذا النمط تلقائيًا استنادًا إلى القيمة المناسبة. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | يحصل على/يحدد اسم النمط الذي يعتمد عليه هذا النمط. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | صحيح إذا كان هذا النمط أحد الأنماط المضمنة في MS Word. |
| [Document](../../aspose.words/style/document/) { get; } | يحصل على مستند المالك. |
| [Font](../../aspose.words/style/font/) { get; } | يحصل على تنسيق الأحرف للنمط. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | صحيح عندما يكون النمط أحد أنماط العناوين المضمنة. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | يحدد ما إذا كان سيتم عرض هذا النمط في معرض الأنماط السريعة داخل واجهة مستخدم MS Word. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; set; } | يحصل على/يحدد اسم`Style` مرتبط بهذا. يُرجع سلسلة فارغة إذا لم تكن هناك أنماط مرتبطة. |
| [List](../../aspose.words/style/list/) { get; } | يحصل على القائمة التي تحدد تنسيق نمط القائمة هذا. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة. |
| [Locked](../../aspose.words/style/locked/) { get; set; } | يحدد ما إذا كان هذا النمط مقفلاً. |
| [Name](../../aspose.words/style/name/) { get; set; } | يحصل على اسم النمط أو يعينه. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | يحصل على/يحدد اسم النمط الذي سيتم تطبيقه تلقائيًا على فقرة جديدة مدرجة بعد فقرة a بتنسيق النمط المحدد. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | يحصل على تنسيق الفقرة للنمط. |
| [Priority](../../aspose.words/style/priority/) { get; set; } | يحصل على/يعين قيمة العدد الصحيح التي تمثل الأولوية لفرز الأنماط في جزء مهام الأنماط. |
| [SemiHidden](../../aspose.words/style/semihidden/) { get; set; } | يحصل/يحدد ما إذا كان النمط مخفيًا من معرض الأنماط ومن جزء مهام الأنماط. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | يحصل على معرف النمط المستقل عن الإعدادات المحلية للنمط المضمن. |
| [Styles](../../aspose.words/style/styles/) { get; } | يحصل على مجموعة الأنماط التي ينتمي إليها هذا النمط. |
| [Type](../../aspose.words/style/type/) { get; } | يحصل على نوع النمط (فقرة أو حرف). |
| [UnhideWhenUsed](../../aspose.words/style/unhidewhenused/) { get; set; } | يحصل/يحدد ما إذا كان النمط المستخدم في المستند الحالي يظهر من معرض الأنماط ومن جزء مهام الأنماط. صحيح عندما يجب إظهار النمط المستخدم في معرض الأنماط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(*Style*) | تتم المقارنة مع النمط المحدد. تتم مقارنة إعدادات الأنماط للأنماط المضمنة فقط. لا يتم تضمين الإعدادات الافتراضية للأنماط في المقارنة. تتم مقارنة النمط الأساسي والنمط المرتبط ونمط الفقرة التالية بشكل متكرر. |
| [Remove](../../aspose.words/style/remove/)() | يزيل النمط المحدد من المستند. |

## أمثلة

يوضح كيفية إنشاء نمط الفقرة واستخدامه مع تنسيق القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء نمط فقرة مخصص.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// قم بإنشاء قائمة وتأكد من أن الفقرات التي تستخدم هذا النمط سوف تستخدم هذه القائمة.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// قم بتطبيق نمط الفقرة على الفقرة الحالية في منشئ المستند، ثم أضف بعض النص.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// قم بتغيير نمط منشئ المستندات إلى نمط لا يحتوي على تنسيق القائمة واكتب فقرة أخرى.
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
//إعادة تعريف النمط تلقائيًا.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق أحد الأنماط الموجودة في المستند على الفقرة التي يقوم منشئ المستند بإنشائها.
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
