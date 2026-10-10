---
title: "طريقة Aspose::Words::Document::get_ShowGrammaticalErrors"
linktitle: "get_ShowGrammaticalErrors"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_ShowGrammaticalErrors. تحدد ما إذا كان سيتم عرض أخطاء القواعد النحوية في هذا المستند في C++."
type: docs
weight: 50000
url: /ar/cpp/aspose.words/document/get_showgrammaticalerrors/
---
## Document::get_ShowGrammaticalErrors method


يحدد ما إذا كان سيتم عرض أخطاء القواعد النحوية في هذا المستند.

```cpp
bool Aspose::Words::Document::get_ShowGrammaticalErrors()
```


## أمثلة



يظهر كيفية إظهار/إخفاء الأخطاء في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج جملتين تحتويان على أخطاء سيتم اكتشافها
// بواسطة مدققي الإملاء والنحو في Microsoft Word.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// إذا تم تمكين هذه الخيارات، فستُخطّ الأخطاء الإملائية
// في المستند الناتج بخط أحمر متعرّج، وسيُبرز خط أزرق مزدوج الأخطاء النحوية.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
