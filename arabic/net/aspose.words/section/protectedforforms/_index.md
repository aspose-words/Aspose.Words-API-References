---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية ProtectedForForms في Microsoft Word على تعزيز أمان المستندات، مما يسمح للمستخدمين بتحرير حقول النماذج المخصصة فقط بسهولة.
type: docs
weight: 60
url: /ar/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

صحيح إذا كان القسم محميًا للنماذج. عند حماية القسم للنماذج، يمكن للمستخدمين تحديد وتعديل النص فقط في حقول النموذج في مايكروسوفت وورد.

```csharp
public bool ProtectedForForms { get; set; }
```

## أمثلة

يوضح كيفية إيقاف الحماية لقسم ما.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// تطبيق الحماية ضد الكتابة على كل قسم في المستند.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// قم بإيقاف تشغيل الحماية ضد الكتابة للقسم الأول.
doc.Sections[0].ProtectedForForms = false;

// في وثيقة الإخراج هذه، سنكون قادرين على تحرير القسم الأول بحرية،
// ولن نتمكن من تحرير محتويات حقل النموذج إلا في القسم الثاني.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
