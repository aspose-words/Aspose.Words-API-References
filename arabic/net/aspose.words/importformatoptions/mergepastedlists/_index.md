---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words لـ .NET
description: دمج قوائم التحكم باستخدام خاصية ImportFormatOptions MergePastedLists. إدارة القوائم الملصقة بسهولة لتحسين تنسيق المستندات. الافتراضي: خطأ.
type: docs
weight: 70
url: /ar/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

يحصل على قيمة منطقية تحدد ما إذا كانت القوائم الملصقة سيتم دمجها مع القوائم المحيطة أم لا. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool MergePastedLists { get; set; }
```

## أمثلة

يوضح كيفية دمج القوائم من المستندات.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// قم بتعيين الخاصية "MergePastedLists" إلى "true"، سيتم دمج القوائم الملصقة مع القوائم المحيطة.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### أنظر أيضا

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
