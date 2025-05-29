---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldDocVariable VariableName لإدارة متغيرات المستندات بسهولة. بسّط استرجاعها وحسّن إدارة مستنداتك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

يحصل على اسم متغير المستند الذي سيتم استرداده أو يعينه.

```csharp
public string VariableName { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول DOCPROPERTY لعرض خصائص المستند والمتغيرات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لاستخدام حقول DOCPROPERTY.
// 1 - عرض خاصية مضمنة:
// قم بتعيين قيمة مخصصة لخاصية "الفئة" المضمنة، ثم قم بإدراج حقل DOCPROPERTY الذي يشير إليها.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 - عرض متغير مستند مخصص:
// قم بتعريف متغير مخصص، ثم قم بالإشارة إلى هذا المتغير باستخدام حقل DOCPROPERTY.
Assert.AreEqual(0, doc.Variables.Count);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### أنظر أيضا

* class [FieldDocVariable](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
