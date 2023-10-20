---
title: PlainTextDocument
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words لـ .NET
description: PlainTextDocument البناء. إنشاء مستند نصي عادي من ملف. يكتشف تنسيق الملف تلقائيًا في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(*string*) {#constructor_2}

إنشاء مستند نصي عادي من ملف. يكتشف تنسيق الملف تلقائيًا.

```csharp
public PlainTextDocument(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم الملف المراد استخراج النص منه. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | لم يتم التعرف على تنسيق المستند أو أنه غير مدعوم. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | توجد مشكلة في المستند ويجب إبلاغ مطوري Aspose.Words بها. |
| IOException | هناك استثناء الإدخال/الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | المستند مشفر ويتطلب كلمة مرور لفتحه، ولكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentException | لا يمكن أن يكون اسم الملف سلسلة فارغة أو فارغة. |

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

* class [PlainTextDocument](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## PlainTextDocument(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_3}

إنشاء مستند نصي عادي من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم الملف المراد استخراج النص منه. |
| loadOptions | LoadOptions | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن ان يكون`باطل`. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | لم يتم التعرف على تنسيق المستند أو أنه غير مدعوم. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | توجد مشكلة في المستند ويجب إبلاغ مطوري Aspose.Words بها. |
| IOException | هناك استثناء الإدخال/الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | المستند مشفر ويتطلب كلمة مرور لفتحه، ولكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentException | لا يمكن أن يكون اسم الملف سلسلة فارغة أو فارغة. |

## أمثلة

يوضح كيفية تحميل محتويات مستند Microsoft Word المشفر بنص عادي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### أنظر أيضا

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream*) {#constructor}

إنشاء مستند نصي عادي من الدفق. يكتشف تنسيق الملف تلقائيًا.

```csharp
public PlainTextDocument(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي يتم استخراج النص منه. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | لم يتم التعرف على تنسيق المستند أو أنه غير مدعوم. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | توجد مشكلة في المستند ويجب إبلاغ مطوري Aspose.Words بها. |
| IOException | هناك استثناء الإدخال/الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | المستند مشفر ويتطلب كلمة مرور لفتحه، ولكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentNullException | لا يمكن أن يكون الدفق فارغًا. |
| NotSupportedException | الدفق لا يدعم القراءة أو البحث. |
| ObjectDisposedException | الدفق هو كائن تم التخلص منه. |

## ملاحظات

يجب تخزين المستند في بداية الدفق. يجب أن يدعم الدفق تحديد المواقع العشوائية.

## أمثلة

يوضح كيفية تحميل محتويات مستند Microsoft Word بنص عادي باستخدام الدفق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### أنظر أيضا

* class [PlainTextDocument](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_1}

إنشاء مستند نصي عادي من الدفق. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي يتم استخراج النص منه. |
| loadOptions | LoadOptions | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن ان يكون`باطل`. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | لم يتم التعرف على تنسيق المستند أو أنه غير مدعوم. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | توجد مشكلة في المستند ويجب إبلاغ مطوري Aspose.Words بها. |
| IOException | هناك استثناء الإدخال/الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | المستند مشفر ويتطلب كلمة مرور لفتحه، ولكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentNullException | لا يمكن أن يكون الدفق فارغًا. |
| NotSupportedException | الدفق لا يدعم القراءة أو البحث. |
| ObjectDisposedException | الدفق هو كائن تم التخلص منه. |

## ملاحظات

يجب تخزين المستند في بداية الدفق. يجب أن يدعم الدفق تحديد المواقع العشوائية.

## أمثلة

يوضح كيفية تحميل محتويات مستند Microsoft Word المشفر في نص عادي باستخدام الدفق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### أنظر أيضا

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
