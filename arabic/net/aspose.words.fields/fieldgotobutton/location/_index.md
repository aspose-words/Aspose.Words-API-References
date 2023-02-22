---
title: FieldGoToButton.Location
second_title: Aspose.Words لمراجع .NET API
description: FieldGoToButton ملكية. الحصول على أو تعيين اسم إشارة مرجعية أو رقم صفحة أو عنصر آخر للانتقال إليه.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

الحصول على أو تعيين اسم إشارة مرجعية أو رقم صفحة أو عنصر آخر للانتقال إليه.

```csharp
public string Location { get; set; }
```

### أمثلة

يظهر لإدراج حقل GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف حقل GOTOBUTTON. عندما ننقر نقرًا مزدوجًا فوق هذا الحقل في Microsoft Word ،
// سيأخذ مؤشر النص إلى الإشارة المرجعية التي يشير اسمها إلى خاصية الموقع.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// أدخل إشارة مرجعية صالحة للحقل للرجوع إليها.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### أنظر أيضا

* class [FieldGoToButton](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldgotobutton/)
* المجسم [Aspose.Words](../../../)


