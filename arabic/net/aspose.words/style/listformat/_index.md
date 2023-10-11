---
title: Style.ListFormat
second_title: Aspose.Words لمراجع .NET API
description: Style ملكية. يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة.
type: docs
weight: 110
url: /ar/net/aspose.words/style/listformat/
---
## Style.ListFormat property

يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة.

```csharp
public ListFormat ListFormat { get; }
```

### ملاحظات

هذه الخاصية صالحة فقط لأنماط الفقرة. بالنسبة لأنواع الأنماط الأخرى، تُرجع هذه الخاصية`باطل`.

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

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Style](../)
* مساحة الاسم [Aspose.Words](../../style/)
* المجسم [Aspose.Words](../../../)


