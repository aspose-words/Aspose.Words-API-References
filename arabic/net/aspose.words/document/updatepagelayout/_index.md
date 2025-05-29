---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words لـ .NET
description: قم بتجديد بنية مستندك باستخدام طريقة UpdatePageLayout، مما يضمن لك الحصول على تخطيط مصقول ومنظم لتحسين قابلية القراءة والعرض.
type: docs
weight: 830
url: /ar/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

إعادة بناء تخطيط الصفحة للمستند.

```csharp
public void UpdatePageLayout()
```

## ملاحظات

تُنسّق هذه الطريقة المستند إلى صفحات وتُحدّث حقول أرقام الصفحات فيه، مثل PAGE وPAGES وPAGEREF وREF. معلومات تخطيط الصفحة المُحدّثة ضرورية لعرض تنسيقات document بشكل صحيح إلى تنسيقات الصفحات الثابتة.

يتم استدعاء هذه الطريقة تلقائيًا عند تحويل مستند إلى PDF أو XPS أو صورة أو طباعته لأول مرة. ومع ذلك، إذا عدّلت المستند بعد عرضه ثم حاولت عرضه مرة أخرى، فلن يُحدّث Aspose.Words تخطيط الصفحة تلقائيًا. في هذه الحالة، يجب عليك استدعاء`UpdatePageLayout` before يتم عرضه مرة أخرى.

## أمثلة

يُظهر متى يجب إعادة حساب تخطيط الصفحة للمستند.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// سيتم حفظ المستند بتنسيق PDF، أو إلى صورة، أو طباعته لأول مرة تلقائيًا
// تخزين تخطيط المستند داخل صفحاته.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

//تعديل المستند بطريقة ما.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// في الإصدار الحالي من Aspose.Words، لا يؤدي تعديل المستند إلى إعادة البناء تلقائيًا
// تخطيط الصفحة المُخزّن مؤقتًا. إذا أردنا تخطيطًا مُخزّنًا مؤقتًا
//للبقاء على اطلاع، سوف نحتاج إلى تحديثه يدويًا.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
