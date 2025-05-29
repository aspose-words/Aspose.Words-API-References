---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.PlainTextDocument لاستخراج النص العادي واستخدامه بسهولة من مستنداتك لتحسين قابلية القراءة والمعالجة.
type: docs
weight: 5170
url: /ar/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

يسمح باستخراج تمثيل نص عادي لمحتوى المستند.

لمعرفة المزيد، قم بزيارة[العمل مع مستند نصي](https://docs.aspose.com/words/net/working-with-text-document/) مقالة توثيقية.

```csharp
public class PlainTextDocument
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | يُنشئ مستند نص عادي من مصدر. يكتشف تنسيق الملف تلقائيًا. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | يُنشئ مستند نص عادي من ملف. يكتشف تنسيق الملف تلقائيًا. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يُنشئ مستند نص عادي من مصدر. يسمح بتحديد خيارات إضافية، مثل كلمة مرور التشفير. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يُنشئ مستند نص عادي من ملف. يسمح بتحديد خيارات إضافية، مثل كلمة مرور التشفير. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | يحصل[`BuiltInDocumentProperties`](./builtindocumentproperties/) من الوثيقة. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | يحصل[`CustomDocumentProperties`](./customdocumentproperties/) من الوثيقة. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | يحصل على محتوى نصي للمستند مُدمجًا كسلسلة. |

## أمثلة

يوضح كيفية تحميل محتويات مستند Microsoft Word في نص عادي.

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
