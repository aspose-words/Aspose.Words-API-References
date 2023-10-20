---
title: FieldSymbol.CharacterCode
linktitle: CharacterCode
articleTitle: CharacterCode
second_title: Aspose.Words لـ .NET
description: FieldSymbol CharacterCode ملكية. الحصول على قيمة نقطة رمز الحرف أو تعيينها بالنظام العشري أو الست عشري في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldsymbol/charactercode/
---
## FieldSymbol.CharacterCode property

الحصول على قيمة نقطة رمز الحرف أو تعيينها بالنظام العشري أو الست عشري.

```csharp
public string CharacterCode { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل الرمز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لاستخدام حقل الرمز لعرض حرف واحد.
// 1 - أضف حقل SYMBOL الذي يعرض رمز © (حقوق الطبع والنشر)، المحدد بواسطة رمز حرف ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// رمز حرف ANSI "U+00A9"، أو "169" في شكل عدد صحيح، محجوز لرمز حقوق الطبع والنشر.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - أضف حقل SYMBOL الذي يعرض رمز ∞ (اللانهاية) وتعديل مظهره:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// في Unicode، يحتل رمز اللانهاية الرمز "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// قم بتغيير خط الرمز الخاص بنا بعد استخدام Windows Character Map
// للتأكد من أن الخط يمكن أن يمثل هذا الرمز.
field.FontName = "Calibri";
field.FontSize = "24";

// يمكننا تعيين هذه العلامة للرموز الطويلة حتى لا تدفع بقية النص الموجود على سطرها للأسفل.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - أضف حقل SYMBOL الذي يعرض الحرف あ،
// بخط يدعم صفحة الرموز Shift-JIS (Windows-932):
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
