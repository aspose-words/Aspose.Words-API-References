---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية XlsxSaveOptions SectionMode على تحسين معالجة القسم لصادرات XLSX، مما يضمن إدارة سلسة للمستندات وأوراق العمل المتعددة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

يحصل على أو يحدد الطريقة التي يتم بها التعامل مع الأقسام عند الحفظ في مستند XLSX الناتج. القيمة الافتراضية هيMultipleWorksheets .

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

## أمثلة

يوضح كيفية حفظ المستند كأوراق عمل منفصلة.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

//سيتم إنشاء كل قسم من المستند على هيئة ورقة عمل منفصلة.
//استخدم 'SingleWorksheet' لعرض كافة المستندات على ورقة عمل واحدة.
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### أنظر أيضا

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
