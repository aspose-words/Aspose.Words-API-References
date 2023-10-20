---
title: FieldHyperlink.Address
linktitle: Address
articleTitle: Address
second_title: Aspose.Words لـ .NET
description: FieldHyperlink Address ملكية. الحصول على الموقع الذي ينتقل إليه هذا الارتباط التشعبي أو تعيينه في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldhyperlink/address/
---
## FieldHyperlink.Address property

الحصول على الموقع الذي ينتقل إليه هذا الارتباط التشعبي أو تعيينه.

```csharp
public string Address { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول HYPERLINK للارتباط بالمستندات الموجودة في نظام الملفات المحلي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// عندما ننقر على حقل الارتباط التشعبي هذا في Microsoft Word،
// سيتم فتح المستند المرتبط ثم وضع المؤشر على الإشارة المرجعية المحددة.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// عندما ننقر على حقل الارتباط التشعبي هذا في Microsoft Word،
// سيفتح المستند المرتبط، وينتقل تلقائيًا لأسفل إلى إطار iframe المحدد.
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
