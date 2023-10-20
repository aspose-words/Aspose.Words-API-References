---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words لـ .NET
description: PclSaveOptions AddPrinterFont طريقة. إضافة معلومات حول الخط الذي تم تحميله إلى الطابعة من قبل الشركة المصنعة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

إضافة معلومات حول الخط الذي تم تحميله إلى الطابعة من قبل الشركة المصنعة.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fontFullName | String | الاسم الكامل للخط (على سبيل المثال "Times New Roman Bold Italic"). |
| fontPclName | String | اسم الخط المستخدم في مستند Pcl. |

## ملاحظات

هناك 52 خطًا سيتم إنشاؤها في أي طابعة وفقًا لمواصفات Pcl. ومع ذلك، يمكن للشركات المصنعة إضافة بعض الخطوط الأخرى إلى أجهزتها.

## أمثلة

يوضح كيفية جعل الطابعة تستبدل كافة مثيلات خط معين بخط مختلف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// عند طباعة هذا المستند، ستستخدم الطابعة الخط "Courier New".
// للوصول إلى الأماكن التي استخدمت فيها وثيقتنا الخط "Courier".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### أنظر أيضا

* class [PclSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
