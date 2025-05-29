---
title: HtmlSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية HtmlSaveOptions ReplaceBackslashWithYenSign مخرجات HTML بتحويل الشرطة المائلة العكسية إلى علامات ين. افتراضيًا، خطأ.
type: docs
weight: 420
url: /ar/net/aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/
---
## HtmlSaveOptions.ReplaceBackslashWithYenSign property

يحدد ما إذا كان يجب استبدال أحرف الشرطة العكسية بعلامات الين. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## ملاحظات

افتراضيًا، يحاكي Aspose.Words سلوك MS Word ولا يستبدل الشرطة المائلة العكسية بعلامات الين في مستندات HTML المُولّدة بواسطة . مع ذلك، كانت الإصدارات السابقة من Aspose.Words تُجري مثل هذه الاستبدالات في بعض سيناريوهات . تُمكّن هذه العلامة التوافق مع الإصدارات السابقة من Aspose.Words.

## أمثلة

يوضح كيفية استبدال أحرف الشرطة المائلة العكسية بعلامات الين (Html).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// بشكل افتراضي، يحاكي Aspose.Words سلوك MS Word ولا يستبدل أحرف الشرطة المائلة العكسية بعلامات الين في
// مستندات HTML المُولَّدة. مع ذلك، كانت الإصدارات السابقة من Aspose.Words تُجري مثل هذه الاستبدالات في بعض
// السيناريوهات. يُمكّن هذا العلم التوافق مع الإصدارات السابقة من Aspose.Words.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
