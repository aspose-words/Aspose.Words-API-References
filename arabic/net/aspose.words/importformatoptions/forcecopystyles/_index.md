---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words لـ .NET
description: ImportFormatOptions ForceCopyStyles ملكية. الحصول على قيمة منطقية أو تعيينها تشير إما إلى نسخ الأنماط المتعارضة فيKeepSourceFormatting mode. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 30
url: /ar/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

الحصول على قيمة منطقية أو تعيينها تشير إما إلى نسخ الأنماط المتعارضة فيKeepSourceFormatting mode. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## ملاحظات

افتراضيًا، إذا كان النمط المطابق موجودًا بالفعل في المستند الوجهة، فسيتم توسيع تنسيق النمط المصدر formatting إلى سمات العقدة المباشرة ويتم إعادة تعيين نمط هذه العقدة إلى الوضع الافتراضي.

عندما يتم ضبط هذا الخيار على`حقيقي`، سيتم نسخ النمط المصدر بالقوة إلى مستند الوجهة باسم فريد وتطبيقه على العقدة المستوردة.

لاحظ أنه في هذه الحالة ليس من المضمون الحفاظ على تنسيق العقدة المستوردة في الوجهة document .

## أمثلة

يوضح كيفية نسخ أنماط المصدر بأسماء فريدة قسرا.

```csharp
// يحتوي كلا المستندين على MyStyle1 وMyStyle2، MyStyle3 موجود فقط في المستند المصدر.
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.AreEqual(paras[0].ParagraphFormat.Style.Name, "MyStyle1_0");
Assert.AreEqual(paras[1].ParagraphFormat.Style.Name, "MyStyle2_0");
Assert.AreEqual(paras[2].ParagraphFormat.Style.Name, "MyStyle3");
```

### أنظر أيضا

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
