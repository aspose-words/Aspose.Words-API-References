---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words XlsxSectionMode enum على تحسين حفظ المستندات بتنسيق XLSX، مما يعزز سير عملك وإدارة المستندات.
type: docs
weight: 6530
url: /ar/net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

يحدد كيفية التعامل مع الأقسام عند حفظ مستند بتنسيق XLSX.

```csharp
public enum XlsxSectionMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| MultipleWorksheets | `0` | يحدد أنه سيتم إنشاء ورقة عمل منفصلة لكل قسم من المستند. |
| SingleWorksheet | `1` | يحدد أنه سيتم حفظ جميع أقسام المستند في ورقة عمل واحدة. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
