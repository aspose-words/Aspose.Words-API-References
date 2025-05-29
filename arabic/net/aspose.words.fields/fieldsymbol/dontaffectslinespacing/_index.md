---
title: FieldSymbol.DontAffectsLineSpacing
linktitle: DontAffectsLineSpacing
articleTitle: DontAffectsLineSpacing
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تتحكم خاصية "رمز الحقل" (FieldSymbol DontAffectsLineSpacing) في تأثير الأحرف على تباعد أسطر الفقرات. حسّن تنسيق مستندك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldsymbol/dontaffectslinespacing/
---
## FieldSymbol.DontAffectsLineSpacing property

يحصل على أو يعين ما إذا كان الحرف الذي تم استرداده بواسطة الحقل يؤثر على تباعد أسطر الفقرة.

```csharp
public bool DontAffectsLineSpacing { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل الرمز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لاستخدام حقل الرمز لعرض حرف واحد.
// 1 - أضف حقل رمز يعرض رمز © (حقوق الطبع والنشر)، المحدد بواسطة رمز حرف ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// رمز الحرف ANSI "U+00A9"، أو "169" في شكل عدد صحيح، مخصص لرمز حقوق النشر.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - أضف حقل رمز يعرض رمز ∞ (اللانهاية)، وقم بتعديل مظهره:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// في Unicode، يحتل رمز اللانهاية الكود "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// تغيير خط رمزنا بعد استخدام خريطة أحرف Windows
// للتأكد من أن الخط يمكنه تمثيل هذا الرمز.
field.FontName = "Calibri";
field.FontSize = "24";

// يمكننا تعيين هذا العلم للرموز الطويلة حتى لا تضغط على بقية النص الموجود على سطرها.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - أضف حقل الرمز الذي يعرض الحرف あ،
// مع الخط الذي يدعم صفحة أكواد Shift-JIS (Windows-932):
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### أنظر أيضا

* class [FieldSymbol](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
