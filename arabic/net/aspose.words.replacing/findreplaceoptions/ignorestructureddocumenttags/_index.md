---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
linktitle: IgnoreStructuredDocumentTags
articleTitle: IgnoreStructuredDocumentTags
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FindReplaceOptions IgnoreStructuredDocumentTags. تحكّم في تجاهل محتوى StructuredDocumentTag باستخدام هذا الإعداد المنطقي سهل الاستخدام.
type: docs
weight: 120
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل محتوى[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

## ملاحظات

عندما يتم تعيين هذا الخيار على`حقيقي` ، محتوى[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) سيتم التعامل مع كنص بسيط.

وإلا،[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) سيتم معالجتها كقصة مستقلة وسيتم البحث عن نمط الاستبدال بشكل منفصل لكل منها[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) ، بحيث إذا عبر النمط عن[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) ، ثم لن يتم إجراء الاستبدال لمثل هذا النمط.

## أمثلة

يوضح كيفية تجاهل محتوى العلامات من الاستبدال.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// تحتوي هذه الفقرة على SDT.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
