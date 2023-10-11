---
title: TxtLoadOptions.DocumentDirection
second_title: Aspose.Words لمراجع .NET API
description: TxtLoadOptions ملكية. الحصول على اتجاه المستند أو تحديده. القيمة الافتراضية هيLeftToRight .
type: docs
weight: 50
url: /ar/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

الحصول على اتجاه المستند أو تحديده. القيمة الافتراضية هيLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

### أمثلة

يوضح كيفية اكتشاف اتجاه نص مستند النص العادي.

```csharp
// قم بإنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل كيفية تحميل مستند نص عادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// قم بتعيين خاصية "DocumentDirection" على "DocumentDirection.Auto" التي يتم اكتشافها تلقائيًا
// اتجاه كل فقرة من النص يقوم Aspose.Words بتحميلها من النص العادي.
// خاصية "Bidi" لكل فقرة ستخزن اتجاهها.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// كشف النص العبري من اليمين إلى اليسار.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// اكتشاف النص الإنجليزي باعتباره من اليمين إلى اليسار.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### أنظر أيضا

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../txtloadoptions/)
* المجسم [Aspose.Words](../../../)


