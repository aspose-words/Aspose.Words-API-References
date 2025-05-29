---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImportFormatOptions ForceCopyStyles، وتحكم بسهولة في نسخ الأنماط في وضع KeepSourceFormatting. القيمة الافتراضية هي "خطأ" للحصول على أفضل النتائج.
type: docs
weight: 30
url: /ar/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

يحصل على قيمة منطقية أو يعينها للإشارة إلى نسخ الأنماط المتضاربة فيKeepSourceFormatting mode. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## ملاحظات

بشكل افتراضي، إذا كان هناك نمط مطابق موجود بالفعل في مستند الوجهة، يتم توسيع نمط المصدر formatting إلى سمات العقدة المباشرة ويتم إعادة تعيين نمط هذه العقدة إلى الوضع الافتراضي.

عندما يتم تعيين هذا الخيار على`حقيقي`سيتم نسخ نمط المصدر قسراً إلى المستند الوجهة باسم فريد وتطبيقه على العقدة المستوردة.

لاحظ أنه في هذه الحالة لا يتم ضمان الحفاظ على تنسيق العقدة المستوردة في المستند الوجهة .

## أمثلة

يوضح كيفية نسخ أنماط المصدر ذات الأسماء الفريدة قسراً.

```csharp
// تحتوي كلتا الوثيقتين على MyStyle1 وMyStyle2، MyStyle3 موجود فقط في مستند المصدر.
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
