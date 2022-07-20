---
title: Style
second_title: Aspose.Words لمراجع .NET API
description: يمثل نمطًا مدمجًا واحدًا أو محددًا بواسطة المستخدم.
type: docs
weight: 5830
url: /ar/net/aspose.words/style/
---
## Style class

يمثل نمطًا مدمجًا واحدًا أو محددًا بواسطة المستخدم.

```csharp
public class Style
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases) { get; } | يحصل على كافة الأسماء المستعارة لهذا النمط. إذا كان النمط لا يحتوي على أسماء مستعارة ، فسيتم إرجاع مصفوفة سلسلة فارغة. |
| [BaseStyleName](../../aspose.words/style/basestylename) { get; set; } | يحصل / يحدد اسم النمط الذي يعتمد عليه هذا النمط. |
| [BuiltIn](../../aspose.words/style/builtin) { get; } | صحيح إذا كان هذا النمط أحد الأنماط المضمنة في MS Word . |
| [Document](../../aspose.words/style/document) { get; } | الحصول على مستند المالك. |
| [Font](../../aspose.words/style/font) { get; } | الحصول على تنسيق الأحرف للنمط. |
| [IsHeading](../../aspose.words/style/isheading) { get; } | صحيح عندما يكون النمط أحد أنماط العناوين المضمنة. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle) { get; set; } | يحدد ما إذا كان هذا النمط سيظهر في معرض الأنماط السريعة داخل واجهة مستخدم MS Word . |
| [LinkedStyleName](../../aspose.words/style/linkedstylename) { get; } | الحصول على اسم النمط المرتبط بهذا النمط. إرجاع سلسلة فارغة إذا لم يتم ربط الأنماط. |
| [List](../../aspose.words/style/list) { get; } | الحصول على القائمة التي تحدد تنسيق نمط القائمة هذا. |
| [ListFormat](../../aspose.words/style/listformat) { get; } | يوفر الوصول إلى خصائص تنسيق القائمة الخاصة بنمط الفقرة. |
| [Name](../../aspose.words/style/name) { get; set; } | الحصول على اسم النمط أو تحديده. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename) { get; set; } | يحصل / يحدد اسم النمط ليتم تطبيقه تلقائيًا على فقرة جديدة مدرجة بعد a فقرة منسقة بالنمط المحدد. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat) { get; } | الحصول على تنسيق الفقرة للنمط. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier) { get; } | الحصول على معرف النمط المستقل للإعدادات المحلية لنمط مضمن. |
| [Styles](../../aspose.words/style/styles) { get; } | الحصول على مجموعة الأنماط التي ينتمي إليها هذا النمط ._ x000d_ |
| [Type](../../aspose.words/style/type) { get; } | الحصول على نوع النمط (فقرة أو حرف) ._ x000d_ |

## طُرق

| اسم | وصف |
| --- | --- |
| [Equals](../../aspose.words/style/equals#equals)(Style) | مقارنة بالنمط المحدد ._ x000d_ تتم مقارنة الأنماط للأنماط المضمنة فقط . لا يتم تضمين افتراضيات الأنماط في المقارنة. تتم مقارنة النمط الأساسي والنمط المرتبط ونمط الفقرة التالي بشكل متكرر. |
| [Remove](../../aspose.words/style/remove)() | يزيل النمط المحدد من المستند. |

### أمثلة

يوضح كيفية إنشاء نمط فقرة واستخدامه مع تنسيق القائمة.

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

// قم بتطبيق نمط الفقرة على الفقرة الحالية لمنشئ الوثيقة ، ثم أضف بعض النص.
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

DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق أحد الأنماط من المستند على الفقرة التي يقوم منشئ المستند بإنشائها.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// قم بإزالة نمطنا المخصص من مجموعة أنماط المستند.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// أي نص يستخدم نمطًا تمت إزالته يعود إلى التنسيق الافتراضي.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->