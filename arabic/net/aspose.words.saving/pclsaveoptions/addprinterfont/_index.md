---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة PclSaveOptions AddPrinterFont لتحميل خطوط الطابعة وإدارتها بكفاءة من الشركات المصنعة لتحسين أداء الطباعة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

يضيف معلومات حول الخط الذي تم تحميله إلى الطابعة بواسطة الشركة المصنعة.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fontFullName | String | الاسم الكامل للخط (على سبيل المثال "Times New Roman Bold Italic"). |
| fontPclName | String | اسم الخط المستخدم في مستند Pcl. |

## ملاحظات

يوجد 52 خطًا يجب بناؤها في أي طابعة وفقًا لمواصفات Pcl. ومع ذلك، يمكن للشركات المصنعة إضافة بعض الخطوط الأخرى إلى أجهزتها.

## أمثلة

يوضح كيفية جعل الطابعة تستبدل جميع مثيلات خط معين بخط مختلف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// عند طباعة هذا المستند، ستستخدم الطابعة الخط "Courier New"
// للوصول إلى الأماكن التي استخدمت فيها مستندنا الخط "Courier".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### أنظر أيضا

* class [PclSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
