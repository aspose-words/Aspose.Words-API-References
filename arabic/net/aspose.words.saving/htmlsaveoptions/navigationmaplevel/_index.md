---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions NavigationMapLevel ملكية. يحدد الحد الأقصى لمستوى العناوين التي يتم ملؤها في خريطة التنقل عند التصدير إلى تنسيقات EPUB أو MOBI أو AZW3 . القيمة الافتراضية هي3  في C#.
type: docs
weight: 390
url: /ar/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

يحدد الحد الأقصى لمستوى العناوين التي يتم ملؤها في خريطة التنقل عند التصدير إلى تنسيقات EPUB، أو MOBI، أو AZW3 . القيمة الافتراضية هي`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## ملاحظات

تتيح خريطة التنقل لوكلاء المستخدم توفير طريقة سهلة للتنقل عبر بنية المستند. عادةً ما تتوافق نقاط التنقل مع العناوين الموجودة في المستند. من أجل ملء العناوين حتى المستوى**ن** قم بتعيين هذه القيمة لـ`NavigationMapLevel`.

افتراضيًا، يتم ملء ثلاثة مستويات من العناوين: فقرات الأنماط**عنوان 1** ,**العنوان 2** و**العنوان 3**. يمكنك تعيين هذه الخاصية إلى قيمة من 1 إلى 9 لطلب المستوى الأقصى المقابل. سيؤدي تعيينها إلى الصفر إلى تقليل خريطة التنقل إلى جذر المستند أو جذور أجزاء المستند فقط.

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
