---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words لـ .NET
description: Aspose.Words.PlainTextDocument فصل. يسمح باستخراج تمثيل النص العادي لمحتوى المستند في C#.
type: docs
weight: 4440
url: /ar/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

يسمح باستخراج تمثيل النص العادي لمحتوى المستند.

لمعرفة المزيد، قم بزيارة[العمل مع مستند نصي](https://docs.aspose.com/words/net/working-with-text-document/) مقالة توثيقية.

```csharp
public class PlainTextDocument
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | إنشاء مستند نصي عادي من الدفق. يكتشف تنسيق الملف تلقائيًا. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | إنشاء مستند نصي عادي من ملف. يكتشف تنسيق الملف تلقائيًا. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | إنشاء مستند نصي عادي من الدفق. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | إنشاء مستند نصي عادي من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | يحصل[`BuiltInDocumentProperties`](./builtindocumentproperties/) من الوثيقة. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | يحصل[`CustomDocumentProperties`](./customdocumentproperties/) من الوثيقة. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | الحصول على المحتوى النصي للمستند متسلسل كسلسلة. |

## أمثلة

يوضح كيفية تحميل محتويات مستند Microsoft Word بنص عادي.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
