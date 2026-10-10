---
title: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName طريقة"
linktitle: "get_FontFileName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName طريقة. يحصل أو يضبط اسم الملف (بدون مسار) الذي سيُحفظ فيه الخط في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/fontsavingargs/get_fontfilename/
---
## FontSavingArgs::get_FontFileName method


يحصل أو يعيّن اسم الملف (بدون المسار) حيث سيتم حفظ الخط.

```cpp
System::String Aspose::Words::Saving::FontSavingArgs::get_FontFileName() const
```

## ملاحظات


تسمح لك هذه الخاصية بإعادة تعريف كيفية إنشاء أسماء ملفات الخطوط أثناء التصدير إلى HTML.

عند إطلاق الحدث، تحتوي هذه الخاصية على اسم الملف الذي أنشأته Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ الخط في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

يقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل خط مضمّن عند التصدير إلى تنسيق HTML. يعتمد كيفية إنشاء اسم ملف الخط على ما إذا كنت تحفظ المستند إلى ملف أو إلى تدفق.

عند حفظ المستند إلى ملف، يبدو اسم ملف الخط المُنشأ مثل *%<document base file name>.<original file name><optional suffix>.<extension>*.

عند حفظ المستند إلى تدفق، يبدو اسم ملف الخط المُنشأ مثل *Aspose.Words.<document guid>.<original file name><optional suffix>.<extension>*.

[FontFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [FontsFolder](../../htmlsaveoptions/get_fontsfolder/) and [FontsFolderAlias](../../htmlsaveoptions/get_fontsfolderalias/) properties.

## انظر أيضًا

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
