---
title: FieldHyperlink.IsImageMap
linktitle: IsImageMap
articleTitle: IsImageMap
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية FieldHyperlink IsImageMap على تحسين خرائط الصور على جانب الخادم من خلال إضافة إحداثيات إلى الارتباطات التشعبية لتحسين الوظائف.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldhyperlink/isimagemap/
---
## FieldHyperlink.IsImageMap property

يحصل على أو يحدد ما إذا كان سيتم إضافة إحداثيات إلى الارتباط التشعبي لخريطة صورة على جانب الخادم.

```csharp
public bool IsImageMap { get; set; }
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
