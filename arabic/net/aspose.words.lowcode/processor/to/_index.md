---
title: Processor.To
linktitle: To
articleTitle: To
second_title: Aspose.Words لـ .NET
description: قم بتحسين سير عملك باستخدام طريقة المعالج لدينا التي تحدد ملفات الإخراج بوضوح، مما يعزز الكفاءة ويبسط مهام إدارة البيانات لديك.
type: docs
weight: 30
url: /ar/net/aspose.words.lowcode/processor/to/
---
## To(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_5}

يحدد ملف الإخراج للمعالج.

```csharp
public Processor To(string output, SaveOptions saveOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| output | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات حفظ اختيارية. في حال عدم تحديدها، يتم تحديد تنسيق الحفظ حسب امتداد الملف. |

### قيمة الإرجاع

إرجاع المعالج بملف الإخراج المحدد.

## ملاحظات

إذا كان الإخراج يتكون من ملفات متعددة، فسيتم استخدام اسم ملف الإخراج المحدد لإنشاء اسم الملف لكل جزء وفقًا للقاعدة: 'outputFile_partIndex.extension'.

## أمثلة

يوضح كيفية تحويل المستندات بسطر واحد من التعليمات البرمجية باستخدام السياق.

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

يوضح كيفية دمج المستندات في مستند إخراج واحد باستخدام السياق.

```csharp
//هناك عدة طرق لدمج المستندات:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## To(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_4}

يحدد ملف الإخراج للمعالج.

```csharp
public Processor To(string output, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| output | String | اسم ملف الإخراج. |
| saveFormat | SaveFormat | حفظ التنسيق. إذا لم يُحدَّد، فسيتم تحديد تنسيق الحفظ حسب امتداد الملف. |

### قيمة الإرجاع

إرجاع المعالج بملف الإخراج المحدد.

## ملاحظات

إذا كان الإخراج يتكون من ملفات متعددة، فسيتم استخدام اسم ملف الإخراج المحدد لإنشاء اسم الملف لكل جزء وفقًا للقاعدة: 'outputFile_partIndex.extension'.

## أمثلة

يوضح كيفية دمج المستندات في مستند إخراج واحد باستخدام السياق.

```csharp
//هناك عدة طرق لدمج المستندات:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## To(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_3}

يحدد تدفق الإخراج للمعالج.

```csharp
public Processor To(Stream output, SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| output | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | حفظ الخيارات. |

### قيمة الإرجاع

إرجاع المعالج مع تدفق الإخراج المحدد.

## ملاحظات

إذا كان الإخراج يتكون من ملفات متعددة، فسيتم حفظ الجزء الأول فقط في التدفق المحدد.

## أمثلة

يوضح كيفية تحويل المستندات من مجرى باستخدام سطر واحد من التعليمات البرمجية باستخدام السياق.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

يوضح كيفية دمج المستندات من التدفق إلى مستند إخراج واحد باستخدام السياق.

```csharp
//هناك عدة طرق لدمج المستندات:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## To(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_2}

يحدد تدفق الإخراج للمعالج.

```csharp
public Processor To(Stream output, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| output | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | حفظ التنسيق. |

### قيمة الإرجاع

إرجاع المعالج مع تدفق الإخراج المحدد.

## ملاحظات

إذا كان الإخراج يتكون من ملفات متعددة، فسيتم حفظ الجزء الأول فقط في التدفق المحدد.

## أمثلة

يوضح كيفية تحويل المستندات من مجرى باستخدام سطر واحد من التعليمات البرمجية باستخدام السياق.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

يوضح كيفية دمج المستندات من التدفق إلى مستند إخراج واحد باستخدام السياق.

```csharp
//هناك عدة طرق لدمج المستندات:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_1}

يحدد قائمة تدفقات المستندات الناتجة.

```csharp
public Processor To(List<Stream> output, SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| output | List`1 | قائمة تدفقات المستندات الناتجة. |
| saveOptions | SaveOptions | حفظ الخيارات. |

### قيمة الإرجاع

إرجاع المعالج بقائمة تدفقات المستندات الناتجة المحددة.

## ملاحظات

إذا كان الإخراج يتكون من ملفات متعددة (مثل الصور أو أجزاء المستند المقسمة)، تتم إضافة مجرى لكل جزء إلى القائمة المحددة. إذا كان الإخراج عبارة عن ملف واحد، تتم إضافة مجرى واحد فقط إلى القائمة. تقع على عاتق المستخدم النهائي مسؤولية التخلص من المجاري التي تم إنشاؤها.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveFormat](../../../aspose.words/saveformat/)*) {#to}

يحدد قائمة تدفقات المستندات الناتجة.

```csharp
public Processor To(List<Stream> output, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| output | List`1 | قائمة تدفقات المستندات الناتجة. |
| saveFormat | SaveFormat | حفظ التنسيق. |

### قيمة الإرجاع

إرجاع المعالج بقائمة تدفقات المستندات الناتجة المحددة.

## ملاحظات

إذا كان الإخراج يتكون من ملفات متعددة (مثل الصور أو أجزاء المستند المقسمة)، تتم إضافة مجرى لكل جزء إلى القائمة المحددة. إذا كان الإخراج عبارة عن ملف واحد، تتم إضافة مجرى واحد فقط إلى القائمة. تقع على عاتق المستخدم النهائي مسؤولية التخلص من المجاري التي تم إنشاؤها.

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
