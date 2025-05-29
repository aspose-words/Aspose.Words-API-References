---
title: XamlFlowSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ReplaceBackslashWithYenSign في XamlFlowSaveOptions تنسيق بياناتك بتحويل الشرطة العكسية إلى علامات ين. افتراضيًا، خطأ.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/xamlflowsaveoptions/replacebackslashwithyensign/
---
## XamlFlowSaveOptions.ReplaceBackslashWithYenSign property

يحدد ما إذا كان يجب استبدال أحرف الشرطة العكسية بعلامات الين. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## ملاحظات

افتراضيًا، يحاكي Aspose.Words سلوك MS Word ولا يستبدل الشرطة المائلة العكسية بعلامات الين في مستندات XAML المُولّدة بواسطة . مع ذلك، كانت الإصدارات السابقة من Aspose.Words تُجري مثل هذه الاستبدالات في بعض سيناريوهات . تُمكّن هذه العلامة التوافق مع الإصدارات السابقة من Aspose.Words.

## أمثلة

يوضح كيفية استبدال أحرف الشرطة المائلة العكسية بعلامات الين (Xaml).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// بشكل افتراضي، يحاكي Aspose.Words سلوك MS Word ولا يستبدل أحرف الشرطة المائلة العكسية بعلامات الين في
// مستندات HTML المُولَّدة. مع ذلك، كانت الإصدارات السابقة من Aspose.Words تُجري مثل هذه الاستبدالات في بعض
// السيناريوهات. يُمكّن هذا العلم التوافق مع الإصدارات السابقة من Aspose.Words.
XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

### أنظر أيضا

* class [XamlFlowSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
