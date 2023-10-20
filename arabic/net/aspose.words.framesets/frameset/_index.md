---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Framesets.Frameset فصل. يمثل صفحة إطارات أو إطارًا واحدًا على صفحة إطارات في C#.
type: docs
weight: 3080
url: /ar/net/aspose.words.framesets/frameset/
---
## Frameset class

يمثل صفحة إطارات أو إطارًا واحدًا على صفحة إطارات.

لمعرفة المزيد، قم بزيارة[البرمجة بالوثائق](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

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
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | الحصول على مجموعة الإطارات الفرعية وصفحات الإطارات. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | الحصول على أو تعيين عنوان URL لصفحة الويب أو اسم ملف المستند لعرضه في هذا الإطار. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كانت صفحة الويب أو اسم ملف المستند محددًا في [`FrameDefaultUrl`](./framedefaulturl/) الخاصية هي مورد خارجي يرتبط به الإطار. |

## ملاحظات

إذا[`ChildFramesets`](./childframesets/) تحتوي الخاصية على عناصر، وهذا المثيل عبارة عن صفحة إطارات، وإلا فهو إطار واحد.

## أمثلة

يوضح كيفية الوصول إلى الإطارات الموجودة على الصفحة.

```csharp
// تحتوي الوثيقة على عدة إطارات مع روابط لمستندات أخرى.
Document doc = new Document(MyDir + "Frameset.docx");

// يمكننا التحقق من عنوان URL الافتراضي (عنوان URL لصفحة ويب أو مستند محلي) أو ما إذا كان الإطار مصدرًا خارجيًا.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx"،
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// تغيير خصائص أحد الإطارات لدينا.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Framesets](../../aspose.words.framesets/)
* المجسم [Aspose.Words](../../)
