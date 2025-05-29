---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words لـ .NET
description: خصّص خاصية DisplayText في FieldGoToButton لتحسين تجربة المستخدم. اضبط نص الزر بسهولة لتنقل سلس في المستندات والوصول السريع.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

يحصل على نص "الزر" الذي يظهر في المستند أو يعينه، بحيث يمكن تحديده لتنشيط القفزة.

```csharp
public string DisplayText { get; set; }
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
