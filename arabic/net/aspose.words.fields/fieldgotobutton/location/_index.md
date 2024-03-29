---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words لـ .NET
description: FieldGoToButton Location ملكية. الحصول على أو تعيين اسم الإشارة المرجعية أو رقم الصفحة أو أي عنصر آخر للانتقال إليه في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

الحصول على أو تعيين اسم الإشارة المرجعية، أو رقم الصفحة، أو أي عنصر آخر للانتقال إليه.

```csharp
public string Location { get; set; }
```

## أمثلة

يظهر لإدراج حقل GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف حقل GOTOBUTTON. عندما ننقر نقرًا مزدوجًا فوق هذا الحقل في Microsoft Word،
// سوف يأخذ مؤشر النص إلى الإشارة المرجعية التي تشير خاصية الموقع إلى اسمها.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// أدخل إشارة مرجعية صالحة للحقل المراد الرجوع إليه.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### أنظر أيضا

* class [FieldGoToButton](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
