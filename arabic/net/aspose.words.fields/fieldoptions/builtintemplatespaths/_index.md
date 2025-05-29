---
title: FieldOptions.BuiltInTemplatesPaths
linktitle: BuiltInTemplatesPaths
articleTitle: BuiltInTemplatesPaths
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة مسارات القالب المضمنة في MS Word باستخدام خاصية FieldOptions BuiltInTemplatesPaths لإنشاء مستندات بسلاسة.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

يحصل على مسارات قوالب MS Word المضمنة أو يعينها.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

## ملاحظات

يتم استخدام هذه الخاصية بواسطة[`FieldAutoText`](../../fieldautotext/) و[`FieldGlossary`](../../fieldglossary/) الحقول، إذا لم يتم العثور على إدخال النص التلقائي المشار إليه في[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) نموذج.

بشكل افتراضي، يقوم MS Word بتخزين القوالب المضمنة في الملفات c:\Users\&lt;username&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx و C:\Users\&lt;username&gt;\AppData\Roaming\Microsoft\Templates\Normal.dotm.

## أمثلة

يوضح كيفية عرض كتلة بناء باستخدام حقول AUTOTEXT وGLOSSARY.

```csharp
Document doc = new Document();

// قم بإنشاء مستند المصطلحات وأضف إليه كتلة بناء النص التلقائي.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// قم بإنشاء مصدر وأضفه كنص إلى كتلة البناء الخاصة بنا.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// قم بتعيين ملف يحتوي على أجزاء قد لا تحتوي عليها مستندنا أو القالب المرفق به.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لاستخدام الحقول لعرض محتويات كتلة البناء الخاصة بنا.
// 1 - استخدام حقل النص التلقائي:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - استخدام حقل المصطلحات:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
