---
title: FieldGlossary.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldGlossary EntryName لإدارة إدخالات القاموس بسهولة - احصل على أسماء أو قم بتعيينها لتحقيق تكامل سلس للمحتوى.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldglossary/entryname/
---
## FieldGlossary.EntryName property

يحصل على اسم إدخال المصطلحات المراد إدراجه أو يعينه.

```csharp
public string EntryName { get; set; }
```

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

* class [FieldGlossary](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
