---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words لـ .NET
description: امسح رؤوس وتذييلات الأقسام بسهولة باستخدام طريقة ClearHeadersFooters. حسّن تصميم مستندك لمظهر أنيق!
type: docs
weight: 120
url: /ar/net/aspose.words/section/clearheadersfooters/
---
## ClearHeadersFooters() {#clearheadersfooters}

مسح رؤوس وتذييلات هذا القسم.

```csharp
public void ClearHeadersFooters()
```

## ملاحظات

تم مسح نص جميع الرؤوس والتذييلات، ولكن[`HeaderFooter`](../../headerfooter/) لا تتم إزالة الأشياء نفسها.

يؤدي هذا إلى ربط رؤوس وتذييلات هذا القسم برؤوس وتذييلات القسم السابق.

## أمثلة

يوضح كيفية مسح محتويات كافة الرؤوس والتذييلات في قسم ما.

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

//إفراغ كافة الرؤوس والتذييلات في هذا القسم من كافة محتوياتها.
// ستظل الرؤوس والتذييلات موجودة ولكن لن يكون هناك شيء لعرضه.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## ClearHeadersFooters(*bool*) {#clearheadersfooters_1}

مسح رؤوس وتذييلات هذا القسم.

```csharp
public void ClearHeadersFooters(bool preserveWatermarks)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| preserveWatermarks | Boolean | صحيح إذا لم تتم إزالة العلامات المائية. |

## ملاحظات

تم مسح نص جميع الرؤوس والتذييلات، ولكن[`HeaderFooter`](../../headerfooter/) لا تتم إزالة الأشياء نفسها.

يؤدي هذا إلى ربط رؤوس وتذييلات هذا القسم برؤوس وتذييلات القسم السابق.

## أمثلة

يوضح كيفية مسح محتويات الرأس والتذييل مع أو بدون علامة مائية.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

//أضف علامة مائية نصية عادية.
doc.Watermark.SetText("Aspose Watermark");

// تأكد من أن الرؤوس والتذييلات تحتوي على محتوى.
HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("First header", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("Second header", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("Third header", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("First footer", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("Second footer", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("Third footer", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

//يزيل كافة محتويات الرأس والتذييل باستثناء العلامات المائية.
doc.FirstSection.ClearHeadersFooters(true);

headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
Assert.AreEqual(WatermarkType.Text, doc.Watermark.Type);

// يزيل كافة محتويات الرأس والتذييل بما في ذلك العلامات المائية.
doc.FirstSection.ClearHeadersFooters(false);
Assert.AreEqual(WatermarkType.None, doc.Watermark.Type);
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
