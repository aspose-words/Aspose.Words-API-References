---
title: FieldOptions.BuiltInTemplatesPaths
second_title: Aspose.Words لمراجع .NET API
description: FieldOptions ملكية. الحصول على أو تعيين مسارات قوالب MS Word المضمنة.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

الحصول على أو تعيين مسارات قوالب MS Word المضمنة.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

### ملاحظات

يتم استخدام هذه الخاصية من قبل[`FieldAutoText`](../../fieldautotext/) و[`FieldGlossary`](../../fieldglossary/) الحقول، إذا لم يتم العثور على إدخال النص التلقائي المشار إليه في[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) نموذج.

افتراضيًا، يقوم برنامج MS Word بتخزين القوالب المضمنة في c:\Users\&lt;username&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx and C:\Users\&lt;username&gt;\ ملفات AppData\Roaming\Microsoft\Templates\Normal.dotm.

### أمثلة

يوضح كيفية عرض الكتلة البرمجية الإنشائية باستخدام حقلي النص التلقائي والمسرد.

```csharp
Document doc = new Document();

// قم بإنشاء مستند معجم وأضف كتلة إنشاء نص تلقائي إليه.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// أنشئ مصدرًا وأضفه كنص إلى الكتلة البرمجية الإنشائية الخاصة بنا.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// قم بتعيين ملف يحتوي على أجزاء قد لا تحتوي عليها وثيقتنا أو القالب المرفق بها.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لاستخدام الحقول لعرض محتويات الكتلة البرمجية الإنشائية الخاصة بنا.
// 1 - استخدام حقل النص التلقائي:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - استخدام حقل المسرد:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldoptions/)
* المجسم [Aspose.Words](../../../)


