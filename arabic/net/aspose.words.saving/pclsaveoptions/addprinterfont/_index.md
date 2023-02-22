---
title: PclSaveOptions.AddPrinterFont
second_title: Aspose.Words لمراجع .NET API
description: PclSaveOptions طريقة. إضافة معلومات حول الخط الذي تم تحميله إلى الطابعة من قبل الشركة المصنعة.
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
| fontFullName | String | الاسم الكامل للخط (على سبيل المثال ، "Times New Roman Bold Italic"). |
| fontPclName | String | اسم الخط المستخدم في مستند Pcl. |

### ملاحظات

هناك 52 خطًا يتم تضمينها في أي طابعة وفقًا لمواصفات Pcl . ومع ذلك يمكن للمصنّعين إضافة بعض الخطوط الأخرى إلى أجهزتهم.

### أمثلة

يوضح كيفية جعل الطابعة تستبدل جميع مثيلات خط معين بخط مختلف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// عند طباعة هذا المستند ، ستستخدم الطابعة الخط "Courier New"
// للوصول إلى الأماكن التي استخدمت فيها وثيقتنا الخط "Courier".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### أنظر أيضا

* class [PclSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pclsaveoptions/)
* المجسم [Aspose.Words](../../../)


