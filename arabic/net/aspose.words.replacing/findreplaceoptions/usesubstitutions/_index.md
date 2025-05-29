---
title: FindReplaceOptions.UseSubstitutions
linktitle: UseSubstitutions
articleTitle: UseSubstitutions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية UseSubstitutions في FindReplaceOptions. فعّل الاستبدالات بسهولة في أنماط الاستبدال لتحسين مرونة تحرير النصوص.
type: docs
weight: 190
url: /ar/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool UseSubstitutions { get; set; }
```

## ملاحظات

للحصول على تفاصيل حول عناصر الاستبدال، يرجى الرجوع إلى: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

## أمثلة

يوضح كيفية التعرف على الاستبدالات واستخدامها ضمن أنماط الاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// إن استخدام الوضع القديم لا يدعم العديد من الميزات المتقدمة، لذا نحتاج إلى تعيينه على "خطأ".
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

يوضح كيفية استبدال النص بالبدائل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط خاصية "UseSubstitutions" على "true" للحصول على
// عملية البحث والاستبدال للتعرف على عناصر الاستبدال.
// قم بضبط خاصية "UseSubstitutions" على "false" لتجاهل عناصر الاستبدال.
options.UseSubstitutions = useSubstitutions;

Regex regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.Range.Replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
    useSubstitutions
        ? "Paul bought a car from John.\rJoe bought a house from Jane."
        : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
