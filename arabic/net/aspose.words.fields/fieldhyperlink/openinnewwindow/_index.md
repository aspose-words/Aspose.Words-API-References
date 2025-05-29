---
title: FieldHyperlink.OpenInNewWindow
linktitle: OpenInNewWindow
articleTitle: OpenInNewWindow
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldHyperlink OpenInNewWindow، وتحكم بسهولة في ما إذا كانت الروابط تفتح في نافذة متصفح جديدة لتحسين تجربة المستخدم.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldhyperlink/openinnewwindow/
---
## FieldHyperlink.OpenInNewWindow property

يحصل على أو يحدد ما إذا كان سيتم فتح موقع الوجهة في نافذة متصفح ويب جديدة.

```csharp
public bool OpenInNewWindow { get; set; }
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
