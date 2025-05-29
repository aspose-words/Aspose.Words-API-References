---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Framesets.Frameset لإدارة إطارات سلسة في المستندات. حسّن صفحات الويب لديك بتكامل إطارات فعال!
type: docs
weight: 3510
url: /ar/net/aspose.words.framesets/frameset/
---
## Frameset class

يمثل صفحة إطارات أو إطارًا واحدًا على صفحة الإطارات.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class Frameset
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Frameset](frameset/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | يحصل على مجموعة من الإطارات الفرعية وصفحات الإطارات. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | يحصل على عنوان URL لصفحة الويب أو اسم ملف المستند الذي سيتم عرضه في هذا الإطار أو يعينه. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان اسم ملف صفحة الويب أو المستند المحدد في [`FrameDefaultUrl`](./framedefaulturl/) الخاصية هي مورد خارجي يرتبط به الإطار. |

## ملاحظات

إذا كان[`ChildFramesets`](./childframesets/) تحتوي الخاصية على عناصر، هذه المثيل عبارة عن صفحة إطارات، وإلا فهي عبارة عن إطار واحد فقط.

## أمثلة

يوضح كيفية الوصول إلى الإطارات الموجودة على الصفحة.

```csharp
//تحتوي الوثيقة على عدة إطارات تحتوي على روابط لوثائق أخرى.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// يمكننا التحقق من عنوان URL الافتراضي (عنوان URL لصفحة ويب أو مستند محلي) أو ما إذا كان الإطار عبارة عن مورد خارجي.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx"،
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// تغيير خصائص أحد إطاراتنا.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Framesets](../../aspose.words.framesets/)
* المجسم [Aspose.Words](../../)
