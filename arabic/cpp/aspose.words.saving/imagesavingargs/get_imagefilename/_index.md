---
title: "طريقة Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName"
linktitle: "get_ImageFileName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName. تحصل أو تعيّن اسم الملف (بدون المسار) حيث سيتم حفظ الصورة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/imagesavingargs/get_imagefilename/
---
## ImageSavingArgs::get_ImageFileName method


يحصل أو يعيّن اسم الملف (بدون المسار) حيث سيتم حفظ الصورة.

```cpp
System::String Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName() const
```

## ملاحظات


هذه الخاصية تسمح لك بإعادة تعريف كيفية إنشاء أسماء ملفات الصور أثناء التصدير إلى HTML.

عند إطلاق الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ الصورة في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

يقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل صورة مضمّنة عند التصدير إلى تنسيق HTML. طريقة إنشاء اسم ملف الصورة تعتمد على ما إذا كنت تحفظ المستند إلى ملف أو إلى دفق.

عند حفظ مستند إلى ملف، يبدو اسم ملف الصورة المُنشأ كالتالي *%<document base file name>.<image number>.<extension>*.

عند حفظ مستند إلى دفق، يبدو اسم ملف الصورة المُنشأ كالتالي *Aspose.Words.<document guid>.<image number>.<extension>*.

[ImageFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to HTML using the document file name, the [ImagesFolder](../../htmlsaveoptions/get_imagesfolder/) and [ImagesFolderAlias](../../htmlsaveoptions/get_imagesfolderalias/) properties.

## انظر أيضًا

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
