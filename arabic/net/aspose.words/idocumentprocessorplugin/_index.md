---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: Aspose.Words لـ .NET
description: اكتشف واجهة Aspose.Words IDocumentProcessorPlugin لتحسين معالجة المستندات لديك باستخدام مكونات إضافية خارجية قوية لتحقيق تكامل سلس.
type: docs
weight: 3610
url: /ar/net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

يحدد واجهة لمكون إضافي لمعالج المستندات الخارجي.

```csharp
public interface IDocumentProcessorPlugin
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | أضف المستند الذي قمت بتحميله باستخدام خيارات التحميل المحددة. |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | قم بتحميل المستند باستخدام خيارات التحميل المحددة. |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | احفظ المستند المحمل بواسطة[`Load`](./load/) الطريقة إلى مجرى الإخراج باستخدام خيارات الحفظ المحددة. |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | يضيف علامة مائية للصورة على كل صفحة من المستند الذي تم تحميله بواسطة[`Load`](./load/) الطريقة. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | يضيف علامة مائية نصية على كل صفحة من المستند الذي تم تحميله بواسطة[`Load`](./load/) الطريقة. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | يقوم بتحليل المستند المحمل بواسطة[`Load`](./load/) الطريقة في[`Document`](../document/) الكائن. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | يحفظ كل صفحة من المستند الذي تم تحميله بواسطة[`Load`](./load/) الطريقة باستخدام خيارات حفظ الصفحة الثابتة المحددة. |

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
