---
title: FieldMacroButton.MacroName
second_title: Aspose.Words لمراجع .NET API
description: FieldMacroButton ملكية. الحصول على أو تعيين اسم الماكرو أو الأمر المراد تشغيله.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

الحصول على أو تعيين اسم الماكرو أو الأمر المراد تشغيله.

```csharp
public string MacroName { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقول MACROBUTTON للسماح لنا بتشغيل وحدات ماكرو للمستند عن طريق النقر فوق.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// أدخل حقل MACROBUTTON ، وقم بالإشارة إلى أحد وحدات الماكرو الخاصة بالمستند بالاسم في خاصية MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// استخدم الخاصية للإشارة إلى "ViewZoom200" ، وهو ماكرو يأتي مع Microsoft Word.
// يمكننا العثور على كافة وحدات الماكرو الأخرى عبر View - >; وحدات الماكرو (القائمة المنسدلة) - >. عرض وحدات الماكرو.
// في تلك القائمة ، حدد "أوامر Word" من القائمة المنسدلة "وحدات الماكرو في:".
// إذا كان وثيقتنا تحتوي على ماكرو مخصص بنفس اسم ماكرو مخزون ،
// سيكون الماكرو الخاص بنا هو الذي يتم تشغيله في حقل MACROBUTTON.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// احفظ المستند كنوع مستند ممكن بماكرو.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### أنظر أيضا

* class [FieldMacroButton](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldmacrobutton/)
* المجسم [Aspose.Words](../../../)


