---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.StyleCollection، التي تتميز بمجموعة غنية من كائنات الأنماط المضمنة والمخصصة لتحسين تنسيق وتصميم مستندك.
type: docs
weight: 6990
url: /ar/net/aspose.words/stylecollection/
---
## StyleCollection class

مجموعة من[`Style`](../style/)الكائنات التي تمثل الأنماط المضمنة والمحددة من قبل المستخدم في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأنماط والموضوعات](https://docs.aspose.com/words/net/working-with-styles-and-themes/) مقالة توثيقية.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | يحصل على عدد الأنماط في المجموعة. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | يحصل على تنسيق النص الافتراضي للمستند. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | يحصل على تنسيق الفقرة الافتراضي للمستند. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | يحصل على مستند المالك. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | يحصل على نمط حسب الاسم أو الاسم المستعار. (3 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | ينشئ نمطًا جديدًا محددًا من قبل المستخدم ويضيفه إلى المجموعة. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | نسخ نمط إلى هذه المجموعة. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | يزيل جميع الأنماط من لوحة معرض الأنماط السريعة. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | يحصل على كائن عدّاد يقوم بإحصاء الأنماط حسب الترتيب الأبجدي لأسمائها. |

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

### أنظر أيضا

* class [Style](../style/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
