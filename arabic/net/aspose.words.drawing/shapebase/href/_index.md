---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase HRef لإدارة عناوين الارتباط التشعبي الكاملة لأشكالك بسهولة، مما يعزز تفاعلية تصميمك ووظائفه.
type: docs
weight: 250
url: /ar/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

يحصل على عنوان الارتباط التشعبي الكامل لشكل ما أو يعينه.

```csharp
public string HRef { get; set; }
```

## ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

فيما يلي أمثلة للقيم الصالحة لهذه الخاصية:

عنوان URI الكامل:`https://www.aspose.com/`.

اسم الملف الكامل:`C:\\مستنداتي\\SalesReport.doc`.

عنوان URI النسبي:`../../../resource.txt`

اسم الملف النسبي:`..\\مستنداتي\\SalesReport.doc`.

وضع إشارة مرجعية داخل مستند آخر:`https://www.aspose.com/Products/Default.aspx#Suites`

وضع إشارة مرجعية داخل هذا المستند:`#اسم_كتاب`.

## أمثلة

يوضح كيفية إدراج شكل يحتوي على صورة، وهو أيضًا ارتباط تشعبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// الضغط على Ctrl + النقر بزر الماوس الأيسر على الشكل في Microsoft Word سيؤدي إلى فتح نافذة متصفح ويب جديدة
// ويأخذنا إلى الرابط التشعبي في خاصية "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
