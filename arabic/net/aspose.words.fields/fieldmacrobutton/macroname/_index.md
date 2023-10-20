---
title: FieldMacroButton.MacroName
linktitle: MacroName
articleTitle: MacroName
second_title: Aspose.Words لـ .NET
description: FieldMacroButton MacroName ملكية. الحصول على اسم الماكرو أو الأمر المراد تشغيله أو تعيينه في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

الحصول على اسم الماكرو أو الأمر المراد تشغيله أو تعيينه.

```csharp
public string MacroName { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول MACROBUTTON للسماح لنا بتشغيل وحدات ماكرو للمستند من خلال النقر.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// قم بإدراج حقل MACROBUTTON، وقم بالإشارة إلى أحد وحدات ماكرو المستند حسب الاسم في خاصية MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// استخدم الخاصية للإشارة إلى "ViewZoom200"، وهو ماكرو يأتي مع Microsoft Word.
// يمكننا العثور على جميع وحدات الماكرو الأخرى عبر طريقة العرض -> وحدات الماكرو (القائمة المنسدلة) -> عرض وحدات الماكرو.
// في تلك القائمة، حدد "أوامر Word" من القائمة المنسدلة "وحدات الماكرو في:".
// إذا كانت وثيقتنا تحتوي على ماكرو مخصص بنفس اسم ماكرو المخزون،
// سيكون الماكرو الخاص بنا هو الذي يتم تشغيله في حقل MACROBUTTON.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// احفظ المستند كنوع مستند يدعم وحدات الماكرو.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### أنظر أيضا

* class [FieldMacroButton](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
