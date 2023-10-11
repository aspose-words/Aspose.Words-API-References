---
title: Class StyleCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.StyleCollection فصل. مجموعة منStyle الكائنات التي تمثل الأنماط المضمنة والمحددة من قبل المستخدم في المستند.
type: docs
weight: 6140
url: /ar/net/aspose.words/stylecollection/
---
## StyleCollection class

مجموعة من[`Style`](../style/) الكائنات التي تمثل الأنماط المضمنة والمحددة من قبل المستخدم في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأنماط والموضوعات](https://docs.aspose.com/words/net/working-with-styles-and-themes/) مقالة توثيقية.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | الحصول على عدد الأنماط في المجموعة. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | الحصول على تنسيق النص الافتراضي للمستند. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | الحصول على تنسيق الفقرة الافتراضي للمستند. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | الحصول على مستند المالك. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | الحصول على النمط بالاسم أو الاسم المستعار. (3 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(StyleType, string) | إنشاء نمط جديد محدد من قبل المستخدم وإضافته إلى المجموعة. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(Style) | لنسخ النمط إلى هذه المجموعة. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | إزالة كافة الأنماط من لوحة Quick Style Gallery. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | الحصول على كائن التعداد الذي سيقوم بتعداد الأنماط بالترتيب الأبجدي لأسمائها. |

### أمثلة

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

### أنظر أيضا

* class [Style](../style/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


