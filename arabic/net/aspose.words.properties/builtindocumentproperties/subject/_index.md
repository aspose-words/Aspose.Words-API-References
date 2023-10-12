---
title: BuiltInDocumentProperties.Subject
second_title: Aspose.Words لمراجع .NET API
description: BuiltInDocumentProperties ملكية. الحصول على أو تعيين موضوع المستند.
type: docs
weight: 260
url: /ar/net/aspose.words.properties/builtindocumentproperties/subject/
---
## BuiltInDocumentProperties.Subject property

الحصول على أو تعيين موضوع المستند.

```csharp
public string Subject { get; set; }
```

### أمثلة

يوضح كيفية العمل مع خصائص المستند المضمنة في فئة "الوصف".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// فيما يلي أربع خصائص مستند مضمنة تحتوي على حقول يمكنها عرض قيمها في نص المستند.
// 1 - خاصية "المؤلف"، والتي يمكننا عرضها باستخدام حقل "المؤلف":
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - خاصية "العنوان"، والتي يمكننا عرضها باستخدام حقل العنوان:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - خاصية "الموضوع"، والتي يمكننا عرضها باستخدام حقل الموضوع:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - خاصية "التعليقات"، والتي يمكننا عرضها باستخدام حقل التعليقات:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// لا تحتوي خاصية "الفئة" المضمنة على حقل يمكنه عرض قيمته.
properties.Category = "My category";

// يمكننا تعيين كلمات رئيسية متعددة للمستند عن طريق فصل قيمة السلسلة لخاصية "الكلمات الرئيسية" بفواصل منقوطة.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// يمكننا النقر بزر الماوس الأيمن فوق هذا المستند في مستكشف Windows والعثور على هذه الخصائص في "الخصائص" -> "تفاصيل".
// الخاصية "المؤلف" المضمنة موجودة في مجموعة "الأصل"، والآخرون موجودون في مجموعة "الوصف".
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../builtindocumentproperties/)
* المجسم [Aspose.Words](../../../)


