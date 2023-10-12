---
title: FindReplaceOptions.UseSubstitutions
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان سيتم التعرف على البدائل واستخدامها ضمن أنماط الاستبدال. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 180
url: /ar/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان سيتم التعرف على البدائل واستخدامها ضمن أنماط الاستبدال. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool UseSubstitutions { get; set; }
```

### ملاحظات

للحصول على تفاصيل حول العناصر البديلة، يرجى الرجوع إلى: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

### أمثلة

يوضح كيفية التعرف على البدائل واستخدامها ضمن أنماط الاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// استخدام الوضع القديم لا يدعم العديد من الميزات المتقدمة، لذا نحتاج إلى ضبطه على "خطأ".
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

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط خاصية "UseSubstitutions" على "صحيح" للحصول عليها
// عملية البحث والاستبدال للتعرف على العناصر البديلة.
// اضبط خاصية "UseSubstitutions" على "خطأ" لتجاهل العناصر البديلة.
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
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


