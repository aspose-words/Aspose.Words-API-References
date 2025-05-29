---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Margins لهوامش مستندات قابلة للتخصيص. حسّن تنسيق مستندك بإعدادات مسبقة سهلة الاستخدام!
type: docs
weight: 4580
url: /ar/net/aspose.words/margins/
---
## Margins enumeration

يحدد الهوامش المحددة مسبقًا.

```csharp
public enum Margins
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Normal | `0` | الهوامش العادية. |
| Narrow | `1` | هوامش ضيقة. |
| Moderate | `2` | هوامش معتدلة. |
| Wide | `3` | هوامش واسعة. |
| Mirrored | `4` | هوامش معكوسة. |
| Custom | `5` | هوامش مخصصة. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
