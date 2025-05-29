---
title: FieldHyperlink.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldHyperlink ScreenTip لتخصيص نص الرابط التشعبي، مما يُحسّن تجربة المستخدم وتفاعله. حسّن روابطك اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldhyperlink/screentip/
---
## FieldHyperlink.ScreenTip property

يحصل على نص تلميح الشاشة للرابط التشعبي أو يعينه.

```csharp
public string ScreenTip { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول HYPERLINK للارتباط بالمستندات الموجودة في نظام الملفات المحلي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// عندما نضغط على حقل الارتباط التشعبي هذا في Microsoft Word،
//سيتم فتح المستند المرتبط ثم وضع المؤشر عند الإشارة المرجعية المحددة.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// عندما نضغط على حقل الارتباط التشعبي هذا في Microsoft Word،
//سيتم فتح المستند المرتبط، والانتقال تلقائيًا إلى الإطار المحدد.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### أنظر أيضا

* class [FieldHyperlink](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
