---
title: FieldGoToButton.DisplayText
second_title: Aspose.Words لمراجع .NET API
description: FieldGoToButton ملكية. الحصول على أو تحديد نص الزر الذي يظهر في المستند  بحيث يمكن تحديده لتنشيط القفزة .
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

الحصول على أو تحديد نص "الزر" الذي يظهر في المستند ، بحيث يمكن تحديده لتنشيط القفزة .

```csharp
public string DisplayText { get; set; }
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


