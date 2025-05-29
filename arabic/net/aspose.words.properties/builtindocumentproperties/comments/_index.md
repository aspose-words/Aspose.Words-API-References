---
title: BuiltInDocumentProperties.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words لـ .NET
description: أدر تعليقات مستنداتك بسهولة مع BuiltInDocumentProperties. احصل على التعليقات أو عيّنها بسهولة لتعزيز التعاون والوضوح.
type: docs
weight: 60
url: /ar/net/aspose.words.properties/builtindocumentproperties/comments/
---
## BuiltInDocumentProperties.Comments property

يحصل على تعليقات المستند أو يعينها.

```csharp
public string Comments { get; set; }
```

## أمثلة

يوضح كيفية العمل مع خصائص المستند المضمنة في فئة "الوصف".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// فيما يلي أربع خصائص مستند مضمنة تحتوي على حقول يمكنها عرض قيمها في نص المستند.
// 1 - خاصية "المؤلف"، والتي يمكننا عرضها باستخدام حقل AUTHOR:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - خاصية "العنوان"، والتي يمكننا عرضها باستخدام حقل TITLE:
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

// لا تحتوي الخاصية المضمنة "الفئة" على حقل يمكنه عرض قيمتها.
properties.Category = "My category";

// يمكننا تعيين كلمات رئيسية متعددة لمستند ما عن طريق فصل قيمة السلسلة الخاصة بخاصية "الكلمات الرئيسية" بفاصلة منقوطة.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// يمكننا النقر بزر الماوس الأيمن على هذا المستند في مستكشف Windows والعثور على هذه الخصائص في "الخصائص" -> "التفاصيل".
//توجد الخاصية المضمنة "المؤلف" في المجموعة "الأصل"، بينما توجد الخاصية الأخرى في المجموعة "الوصف".
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
