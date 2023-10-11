---
title: FieldAutoText.EntryName
second_title: Aspose.Words لمراجع .NET API
description: FieldAutoText ملكية. الحصول على اسم إدخال النص التلقائي أو تعيينه.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldautotext/entryname/
---
## FieldAutoText.EntryName property

الحصول على اسم إدخال النص التلقائي أو تعيينه.

```csharp
public string EntryName { get; set; }
```

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

* class [FieldAutoText](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldautotext/)
* المجسم [Aspose.Words](../../../)


