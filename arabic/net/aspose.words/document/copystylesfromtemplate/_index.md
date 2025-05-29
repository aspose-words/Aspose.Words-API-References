---
title: Document.CopyStylesFromTemplate
linktitle: CopyStylesFromTemplate
articleTitle: CopyStylesFromTemplate
second_title: Aspose.Words لـ .NET
description: انسخ الأنماط بسهولة من القالب الذي اخترته إلى أي مستند باستخدام طريقة CopyStylesFromTemplate، مما يعزز سير عملك واتساق مستندك.
type: docs
weight: 610
url: /ar/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(*string*) {#copystylesfromtemplate_1}

نسخ الأنماط من القالب المحدد إلى مستند.

```csharp
public void CopyStylesFromTemplate(string template)
```

## ملاحظات

عند نسخ الأنماط من قالب إلى مستند، يُعاد تعريف الأنماط ذات الأسماء المشابهة في المستند لتتوافق مع أوصاف الأنماط فيه. تُنسخ الأنماط الفريدة من القالب إلى المستند، مع الحفاظ على ثباتها.

## أمثلة

يوضح كيفية نسخ الأنماط من مستند إلى آخر.

```csharp
// قم بإنشاء مستند، ثم أضف الأنماط التي سنقوم بنسخها إلى مستند آخر.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// قم بإنشاء مستند سنقوم بنسخ الأنماط إليه.
Document target = new Document();

// قم بإنشاء نمط يحمل نفس اسم النمط من مستند القالب وأضفه إلى المستند المستهدف.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// هناك طريقتان لاستدعاء الطريقة لنسخ كافة الأنماط من مستند إلى آخر.
// 1 - تمرير كائن مستند القالب:
target.CopyStylesFromTemplate(template);

// يؤدي نسخ الأنماط إلى إضافة جميع الأنماط من مستند القالب إلى الهدف
// ويستبدل الأنماط الموجودة بنفس الاسم.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - تمرير اسم ملف النظام المحلي لمستند القالب:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(*[Document](../)*) {#copystylesfromtemplate}

نسخ الأنماط من القالب المحدد إلى مستند.

```csharp
public void CopyStylesFromTemplate(Document template)
```

## ملاحظات

عند نسخ الأنماط من قالب إلى مستند، يُعاد تعريف الأنماط ذات الأسماء المشابهة في المستند لتتوافق مع أوصاف الأنماط فيه. تُنسخ الأنماط الفريدة من القالب إلى المستند، مع الحفاظ على ثباتها.

## أمثلة

يوضح كيفية نسخ الأنماط من القالب إلى مستند عبر المستند.

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

يوضح كيفية نسخ الأنماط من مستند إلى آخر.

```csharp
// قم بإنشاء مستند، ثم أضف الأنماط التي سنقوم بنسخها إلى مستند آخر.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// قم بإنشاء مستند سنقوم بنسخ الأنماط إليه.
Document target = new Document();

// قم بإنشاء نمط يحمل نفس اسم النمط من مستند القالب وأضفه إلى المستند المستهدف.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// هناك طريقتان لاستدعاء الطريقة لنسخ كافة الأنماط من مستند إلى آخر.
// 1 - تمرير كائن مستند القالب:
target.CopyStylesFromTemplate(template);

// يؤدي نسخ الأنماط إلى إضافة جميع الأنماط من مستند القالب إلى الهدف
// ويستبدل الأنماط الموجودة بنفس الاسم.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - تمرير اسم ملف النظام المحلي لمستند القالب:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
