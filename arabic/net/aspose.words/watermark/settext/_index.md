---
title: Watermark.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words لـ .NET
description: Watermark SetText طريقة. يضيف علامة مائية نصية إلى المستند في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/watermark/settext/
---
## SetText(*string*) {#settext}

يضيف علامة مائية نصية إلى المستند.

```csharp
public void SetText(string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| text | String | النص الذي يتم عرضه كعلامة مائية. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم العرض عندما يكون طول النص خارج النطاق أو عندما يحتوي النص على مسافات بيضاء فقط. |
| ArgumentNullException | يرمي عندما يكون النص`باطل` . |

## ملاحظات

يجب أن يكون طول النص في النطاق من 1 إلى 200 ضمناً. لا يمكن أن يكون النص`باطل` أو تحتوي على مسافات بيضاء فقط.

## أمثلة

يوضح كيفية إنشاء علامة مائية نصية.

```csharp
Document doc = new Document();

// أضف علامة مائية نصية عادية.
doc.Watermark.SetText("Aspose Watermark");

// إذا أردنا تعديل تنسيق النص باستخدامه كعلامة مائية،
// يمكننا القيام بذلك عن طريق تمرير كائن TextWatermarkOptions عند إنشاء العلامة المائية.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// يمكننا إزالة علامة مائية من مستند مثل هذا.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### أنظر أيضا

* class [Watermark](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## SetText(*string, [TextWatermarkOptions](../../textwatermarkoptions/)*) {#settext_1}

يضيف علامة مائية نصية إلى المستند.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| text | String | النص الذي يتم عرضه كعلامة مائية. |
| options | TextWatermarkOptions | يحدد خيارات إضافية للعلامة المائية النصية. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم العرض عندما يكون طول النص خارج النطاق أو عندما يحتوي النص على مسافات بيضاء فقط. |
| ArgumentNullException | يرمي عندما يكون النص`باطل` . |

## ملاحظات

يجب أن يكون طول النص في النطاق من 1 إلى 200 ضمناً. لا يمكن أن يكون النص`باطل` أو تحتوي على مسافات بيضاء فقط.

لو[`TextWatermarkOptions`](../../textwatermarkoptions/) يكون`باطل`سيتم تعيين العلامة المائية بالخيارات الافتراضية.

## أمثلة

يوضح كيفية إنشاء علامة مائية نصية.

```csharp
Document doc = new Document();

// أضف علامة مائية نصية عادية.
doc.Watermark.SetText("Aspose Watermark");

// إذا أردنا تعديل تنسيق النص باستخدامه كعلامة مائية،
// يمكننا القيام بذلك عن طريق تمرير كائن TextWatermarkOptions عند إنشاء العلامة المائية.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// يمكننا إزالة علامة مائية من مستند مثل هذا.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### أنظر أيضا

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
