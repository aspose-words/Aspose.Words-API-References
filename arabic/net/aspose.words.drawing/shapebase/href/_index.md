---
title: ShapeBase.HRef
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الحصول على عنوان الارتباط التشعبي الكامل للشكل أو تعيينه.
type: docs
weight: 230
url: /ar/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

الحصول على عنوان الارتباط التشعبي الكامل للشكل أو تعيينه.

```csharp
public string HRef { get; set; }
```

### ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

فيما يلي أمثلة للقيم الصالحة لهذه الخاصية:

عنوان URL الكامل:`https://www.aspose.com/`.

اسم الملف الكامل:`C:\\My Documents\\SalesReport.doc`.

معرف الموارد المنتظم (URI) النسبي:`../../../resource.txt`

اسم الملف النسبي:`..\\المستندات\\SalesReport.doc`.

إشارة مرجعية داخل مستند آخر:`https://www.aspose.com/Products/Default.aspx#Suites`

الإشارة المرجعية داخل هذا المستند:`#BookmakName`.

### أمثلة

يوضح كيفية إدراج شكل يحتوي على صورة، ويكون أيضًا ارتباطًا تشعبيًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + النقر بزر الماوس الأيسر على الشكل في Microsoft Word سيفتح نافذة متصفح ويب جديدة
// وانقلنا إلى الارتباط التشعبي الموجود في خاصية "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


