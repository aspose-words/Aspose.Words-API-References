---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: Aspose.Words لـ .NET
description: LayoutOptions ShowHiddenText ملكية. الحصول على أو تعيين الإشارة إلى ما إذا كان سيتم عرض النص المخفي في المستند. الافتراضي هوخطأ شنيع  في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

الحصول على أو تعيين الإشارة إلى ما إذا كان سيتم عرض النص المخفي في المستند. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ShowHiddenText { get; set; }
```

## ملاحظات

تؤثر هذه الخاصية على كافة المحتويات المخفية، وليس النص فقط.

## أمثلة

يوضح كيفية إخفاء النص في مستند الإخراج المقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// أدخل نصًا مخفيًا، ثم حدد ما إذا كنا نرغب في حذفه من المستند المعروض.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### أنظر أيضا

* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
