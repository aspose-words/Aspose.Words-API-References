---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words FramesetCollection، الحل الأمثل لإدارة مثيلات Frameset المتعددة بسهولة أثناء معالجة المستندات.
type: docs
weight: 3520
url: /ar/net/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class

يمثل مجموعة من حالات[`Frameset`](../frameset/) الصف.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class FramesetCollection : IEnumerable<Frameset>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FramesetCollection](framesetcollection/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.framesets/framesetcollection/count/) { get; } | يحصل على عدد الإطارات أو صفحات الإطارات الموجودة في المجموعة. |
| [Item](../../aspose.words.framesets/framesetcollection/item/) { get; } | يحصل على إطار أو إطارات الصفحة عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words.framesets/framesetcollection/getenumerator/)() | يعيد مُعَدِّدًا يتكرر خلال المجموعة. |

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

* class [Frameset](../frameset/)
* مساحة الاسم [Aspose.Words.Framesets](../../aspose.words.framesets/)
* المجسم [Aspose.Words](../../)
