---
title: FieldMacroButton.MacroName
linktitle: MacroName
articleTitle: MacroName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldMacroButton MacroName لإدارة وحدات الماكرو أو الأوامر وتخصيصها بسهولة لتحسين الوظائف والكفاءة.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

يحصل على اسم الماكرو أو الأمر الذي سيتم تشغيله أو يعينه.

```csharp
public string MacroName { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول MACROBUTTON للسماح لنا بتشغيل وحدات الماكرو الخاصة بالمستند عن طريق النقر.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// أدخل حقل MACROBUTTON، ثم قم بالإشارة إلى أحد وحدات الماكرو الموجودة في المستند بالاسم في خاصية MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// استخدم الخاصية للإشارة إلى "ViewZoom200"، وهو ماكرو يأتي مع Microsoft Word.
// يمكننا العثور على جميع وحدات الماكرو الأخرى عبر عرض -> وحدات الماكرو (القائمة المنسدلة) -> عرض وحدات الماكرو.
// في تلك القائمة، حدد "أوامر Word" من القائمة المنسدلة "وحدات الماكرو في:".
// إذا كانت مستندنا تحتوي على ماكرو مخصص يحمل نفس اسم الماكرو المخزن،
// سيكون الماكرو الخاص بنا هو الذي يقوم بتشغيل حقل MACROBUTTON.
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
