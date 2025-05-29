---
title: Style.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية الوصول إلى تنسيق فقرات الأنماط وتخصيصها لتحسين عرض المستندات والتنسيق الاحترافي.
type: docs
weight: 150
url: /ar/net/aspose.words/style/paragraphformat/
---
## Style.ParagraphFormat property

يحصل على تنسيق الفقرة للنمط.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## ملاحظات

بالنسبة لأنماط الأحرف والقوائم، تُرجع هذه الخاصية`باطل`.

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

* class [ParagraphFormat](../../paragraphformat/)
* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
