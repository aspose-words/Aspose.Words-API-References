---
title: "طريقة Aspose::Words::Document::get_GrammarChecked"
linktitle: "get_GrammarChecked"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_GrammarChecked. تُرجع true إذا تم فحص المستند نحويًا في C++."
type: docs
weight: 29000
url: /ar/cpp/aspose.words/document/get_grammarchecked/
---
## Document::get_GrammarChecked method


يعيد **true** إذا تم فحص المستند للنحو.

```cpp
bool Aspose::Words::Document::get_GrammarChecked()
```


## أمثلة



يظهر كيفية ضبط التحقق من الإملاء أو القواعد.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// السلسلة التي تحتوي على أخطاء إملائية.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// يبدأ فحص الإملاء/القواعد إذا ضبطنا الخصائص على false.
// يمكننا رؤية جميع الأخطاء في Microsoft Word عبر Review -> Spelling & Grammar.
// لاحظ أن Microsoft Word لا يبدأ تدقيق القواعد الإملائية تلقائيًا لتنسيق المستند DOC و RTF.
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
