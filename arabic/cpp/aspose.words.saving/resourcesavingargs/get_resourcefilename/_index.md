---
title: "طريقة Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName"
linktitle: "get_ResourceFileName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName. يحصل على أو يضبط اسم الملف (بدون مسار) حيث سيتم حفظ المورد في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/resourcesavingargs/get_resourcefilename/
---
## ResourceSavingArgs::get_ResourceFileName method


يحصل أو يعيّن اسم الملف (بدون المسار) حيث سيتم حفظ المورد.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName() const
```

## ملاحظات


تسمح لك هذه الخاصية بإعادة تعريف طريقة إنشاء أسماء ملفات الموارد أثناء التصدير إلى HTML ثابت الصفحات أو SVG أو Markdown.

عند حدوث الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ المورد في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

يقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل مورد عند التصدير إلى تنسيق HTML ثابت الصفحات أو SVG أو Markdown. تعتمد طريقة إنشاء اسم ملف المورد على ما إذا كنت تحفظ المستند إلى ملف أو إلى تدفق.

عند حفظ المستند إلى ملف، يبدو اسم ملف المورد المُنشأ كالتالي *%<document base file name>.<image number>.<extension>*.

عند حفظ المستند إلى تدفق، يبدو اسم ملف المورد المُنشأ كالتالي *Aspose.Words.<document guid>.<image number>.<extension>*.

[ResourceFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [ResourcesFolder](../../htmlfixedsaveoptions/get_resourcesfolder/) or [ResourcesFolder](../../svgsaveoptions/get_resourcesfolder/) and [ResourcesFolderAlias](../../htmlfixedsaveoptions/get_resourcesfolderalias/) or [ResourcesFolderAlias](../../svgsaveoptions/get_resourcesfolderalias/) or [ImagesFolder](../../markdownsaveoptions/get_imagesfolder/) or [ImagesFolderAlias](../../markdownsaveoptions/get_imagesfolderalias/) properties.

## انظر أيضًا

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
