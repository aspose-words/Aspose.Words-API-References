---
title: Converter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words لـ .NET
description: قم بإنشاء مثيل جديد لمعالج المحول بسهولة باستخدام طريقة Converter Create القوية لدينا لتحويل البيانات بسلاسة.
type: docs
weight: 10
url: /ar/net/aspose.words.lowcode/converter/create/
---
## Create() {#create}

ينشئ مثيلًا جديدًا لمعالج المحول.

```csharp
public static Converter Create()
```

### أنظر أيضا

* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Create(*[ConverterContext](../../convertercontext/)*) {#create_1}

ينشئ مثيلًا جديدًا لمعالج المحول.

```csharp
public static Converter Create(ConverterContext context)
```

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

### أنظر أيضا

* class [ConverterContext](../../convertercontext/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
