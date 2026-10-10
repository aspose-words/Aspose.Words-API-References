---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly"
linktitle: "get_FindWholeWordsOnly"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly. تشير القيمة True إلى أن oldValue يجب أن تكون كلمة مستقلة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True يدل على أن oldValue يجب أن تكون كلمة مستقلة.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## أمثلة



يوضح كيفية تبديل عمليات البحث والاستبدال التي تقتصر على الكلمات المستقلة فقط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// عيّن علم "FindWholeWordsOnly" إلى "true" لاستبدال النص الموجود إذا لم يكن جزءًا من كلمة أخرى.
// عيّن علم "FindWholeWordsOnly" إلى "false" لاستبدال كل النص بغض النظر عن محيطه.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
