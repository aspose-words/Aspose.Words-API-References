---
title: "Метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix"
linktitle: "get_IdPrefix"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix. Указывает префикс, который добавляется ко всем сгенерированным идентификаторам элементов в выходном документе. Значение по умолчанию — null, и в C++ префикс не добавляется."
type: docs
weight: 10500
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/get_idprefix/
---
## HtmlFixedSaveOptions::get_IdPrefix method


Указывает префикс, который добавляется ко всем сгенерированным идентификаторам элементов в выходном документе. Значение по умолчанию — null, и префикс не добавляется.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix() const
```


## Примеры



Показывает, как добавить префикс, который добавляется ко всем сгенерированным идентификаторам элементов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

## См. также

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
