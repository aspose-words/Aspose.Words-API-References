---
title: "Aspose::Words::Saving::SaveOptions::get_TempFolder method"
linktitle: "get_TempFolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::SaveOptions::get_TempFolder method. يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ إلى ملف DOC أو DOCX. بشكل افتراضي، هذه الخاصية هي null ولا يتم استخدام ملفات مؤقتة في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


يحدد المجلد الخاص بالملفات المؤقتة المستخدمة عند الحفظ إلى ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## ملاحظات


عند حفظ Aspose.Words لمستند، يحتاج إلى إنشاء هياكل داخلية مؤقتة. بشكل افتراضي، تُنشأ هذه الهياكل الداخلية في الذاكرة وتزداد استهلاك الذاكرة لفترة قصيرة أثناء حفظ المستند. عند اكتمال الحفظ، يتم تحرير الذاكرة واستعادتها بواسطة جامع القمامة.

تحديد مجلد مؤقت باستخدام [TempFolder](./) سيتسبب في أن يحتفظ Aspose.Words بالهياكل الداخلية في ملفات مؤقتة بدلاً من الذاكرة. هذا يقلل من استهلاك الذاكرة أثناء الحفظ، لكنه سيقلل من أداء الحفظ.

يجب أن يكون المجلد موجودًا وقابلًا للكتابة، وإلا سيتم رمي استثناء.

يقوم Aspose.Words بحذف جميع الملفات المؤقتة تلقائيًا عند اكتمال الحفظ.

## أمثلة



يظهر كيفية استخدام القرص الصلب بدلاً من الذاكرة عند حفظ مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// عند حفظنا لمستند، يتم تخزين عناصر مختلفة مؤقتًا في الذاكرة أثناء عملية الحفظ.
// يمكننا استخدام هذا الخيار لاستخدام مجلد مؤقت في نظام الملفات المحلي بدلاً من ذلك،
// مما سيقلل من استهلاك الذاكرة لتطبيقنا.
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// يجب أن يكون المجلد المؤقت المحدد موجودًا في نظام الملفات المحلي قبل عملية الحفظ.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// سيستمر وجود المجلد دون أي محتويات متبقية من عملية التحميل.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## انظر أيضًا

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
