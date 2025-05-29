---
title: StyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Item القوية في StyleCollection لاسترداد الأنماط بسهولة حسب الاسم أو الاسم المستعار، مما يعزز تجربة التصميم الخاصة بك بسهولة!
type: docs
weight: 50
url: /ar/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

يحصل على نمط حسب الاسم أو الاسم المستعار.

```csharp
public Style this[string name] { get; }
```

## ملاحظات

حساسة لحالة الأحرف، الإرجاع`باطل` إذا لم يتم العثور على النمط بالاسم المحدد.

إذا كان هذا اسمًا إنجليزيًا لنمط مدمج غير موجود بعد، فسيتم إنشائه تلقائيًا.

## أمثلة

يُظهر متى يجب إعادة حساب تخطيط الصفحة للمستند.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// سيتم حفظ المستند بتنسيق PDF، أو إلى صورة، أو طباعته لأول مرة تلقائيًا
// تخزين تخطيط المستند داخل صفحاته.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

//تعديل المستند بطريقة ما.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// في الإصدار الحالي من Aspose.Words، لا يؤدي تعديل المستند إلى إعادة البناء تلقائيًا
// تخطيط الصفحة المُخزّن مؤقتًا. إذا أردنا تخطيطًا مُخزّنًا مؤقتًا
//للبقاء على اطلاع، سوف نحتاج إلى تحديثه يدويًا.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### أنظر أيضا

* class [Style](../../style/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

يحصل على نمط مضمن من خلال معرفه المستقل عن الإعدادات المحلية.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| معامل | وصف |
| --- | --- |
| sti | أ[`StyleIdentifier`](../../styleidentifier/) القيمة التي تحدد النمط المدمج الذي سيتم استرداده. |

## ملاحظات

عند الوصول إلى نمط غير موجود بعد، يتم إنشائه تلقائيًا.

## أمثلة

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// تعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles.DefaultFont.Name = "Courier New";
// إذا أضفنا نمط "StyleType.Paragraph"، ستطبق المجموعة قيم
// خاصية "DefaultParagraphFormat" الخاصة بها إلى خاصية "ParagraphFormat" الخاصة بالنمط.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
//أضف نمطًا، ثم تأكد من أنه يحتوي على الإعدادات الافتراضية.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### أنظر أيضا

* class [Style](../../style/)
* enum [StyleIdentifier](../../styleidentifier/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

يحصل على نمط حسب الفهرس.

```csharp
public Style this[int index] { get; }
```

## أمثلة

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// تعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles.DefaultFont.Name = "Courier New";
// إذا أضفنا نمط "StyleType.Paragraph"، ستطبق المجموعة قيم
// خاصية "DefaultParagraphFormat" الخاصة بها إلى خاصية "ParagraphFormat" الخاصة بالنمط.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
//أضف نمطًا، ثم تأكد من أنه يحتوي على الإعدادات الافتراضية.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### أنظر أيضا

* class [Style](../../style/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
