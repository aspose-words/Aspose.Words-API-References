---
title: "طريقة Aspose::Words::Loading::LoadOptions::get_TempFolder"
linktitle: "get_TempFolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::LoadOptions::get_TempFolder. يسمح باستخدام ملفات مؤقتة عند قراءة المستند. بشكل افتراضي تكون هذه الخاصية null ولا تُستخدم ملفات مؤقتة في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


يسمح باستخدام ملفات مؤقتة عند قراءة المستند. بشكل افتراضي تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## ملاحظات


يجب أن يكون المجلد موجودًا وقابلًا للكتابة، وإلا سيتم رمي استثناء.

يقوم Aspose.Words بحذف جميع الملفات المؤقتة تلقائيًا عند اكتمال القراءة.

## أمثلة



يوضح كيفية تحميل مستند باستخدام ملفات مؤقتة.
```cpp
// لاحظ أن هذا النهج يمكن أن يقلل من استهلاك الذاكرة لكنه يقلل من السرعة.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// تأكد من وجود الدليل ثم حمّل.
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);
```


يوضح كيفية استخدام القرص الصلب بدلاً من الذاكرة عند تحميل مستند.
```cpp
// عند تحميلنا لمستند، يتم تخزين عناصر مختلفة مؤقتًا في الذاكرة أثناء حدوث عملية الحفظ.
// يمكننا استخدام هذا الخيار لاستخدام مجلد مؤقت في نظام الملفات المحلي بدلاً من ذلك،
// مما سيقلل من استهلاك الذاكرة لتطبيقنا.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// يجب أن يكون المجلد المؤقت المحدد موجودًا في نظام الملفات المحلي قبل عملية التحميل.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", options);

// سيستمر وجود المجلد دون أي محتويات متبقية من عملية التحميل.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## انظر أيضًا

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
