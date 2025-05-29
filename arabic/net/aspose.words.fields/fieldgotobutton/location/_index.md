---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية موقع FieldGoToButton، وقم بسهولة بتعيين الإشارات المرجعية أو أرقام الصفحات أو العناصر لضمان التنقل السلس وتحسين تجربة المستخدم.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

يحصل على اسم إشارة مرجعية أو رقم صفحة أو أي عنصر آخر للانتقال إليه أو يعينه.

```csharp
public string Location { get; set; }
```

## أمثلة

يظهر لإدراج حقل GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف حقل GOTOBUTTON. عند النقر المزدوج على هذا الحقل في مايكروسوفت وورد،
//سيتم نقل مؤشر النص إلى الإشارة المرجعية التي يشير إليها خاصية الموقع.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// أدخل إشارة مرجعية صالحة للحقل للإشارة إليه.
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
