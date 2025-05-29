---
title: TxtSaveOptionsBase.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تحسين تصدير النصوص باستخدام خاصية الترميز في TxtSaveOptionsBase. اضبط خيارات الترميز بسهولة لتنسيق نص UTF-8 بسلاسة.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## TxtSaveOptionsBase.Encoding property

يحدد الترميز الذي سيتم استخدامه عند التصدير بتنسيقات نصية. القيمة الافتراضية هي**ترميز UTF8** .

```csharp
public Encoding Encoding { get; set; }
```

## أمثلة

يوضح كيفية تعيين الترميز لمستند الإخراج .txt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف بعض النصوص التي تحتوي على أحرف من خارج مجموعة أحرف ASCII.
builder.Write("À È Ì Ò Ù.");

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// تأكد من أن خاصية "الترميز" تحتوي على الترميز المناسب لمحتويات مستندنا.
Assert.AreEqual(System.Text.Encoding.UTF8, txtSaveOptions.Encoding);

doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

string docText = System.Text.Encoding.UTF8.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt"));

Assert.AreEqual("\uFEFFÀ È Ì Ò Ù.\r\n", docText);

//قد يؤدي استخدام ترميز غير مناسب إلى فقدان محتويات المستند.
txtSaveOptions.Encoding = System.Text.Encoding.ASCII;
doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System.Text.Encoding.ASCII.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt"));

Assert.AreEqual("? ? ? ? ?.\r\n", docText);
```

### أنظر أيضا

* class [TxtSaveOptionsBase](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
