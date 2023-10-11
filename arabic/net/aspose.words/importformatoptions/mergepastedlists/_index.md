---
title: ImportFormatOptions.MergePastedLists
second_title: Aspose.Words لمراجع .NET API
description: ImportFormatOptions ملكية. الحصول على أو تعيين قيمة منطقية تحدد ما إذا كان سيتم دمج القوائم الملصقة مع القوائم المحيطة. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 70
url: /ar/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

الحصول على أو تعيين قيمة منطقية تحدد ما إذا كان سيتم دمج القوائم الملصقة مع القوائم المحيطة. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool MergePastedLists { get; set; }
```

### أمثلة

يوضح كيفية دمج القوائم من المستندات.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// قم بتعيين خاصية "MergePastedLists" على "صحيح"، وسيتم دمج القوائم الملصقة مع القوائم المحيطة.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### أنظر أيضا

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../importformatoptions/)
* المجسم [Aspose.Words](../../../)


