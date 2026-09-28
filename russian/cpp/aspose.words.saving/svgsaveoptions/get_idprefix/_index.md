---
title: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix метод"
linktitle: "get_IdPrefix"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix метод. Указывает префикс, который добавляется ко всем сгенерированным идентификаторам элементов в выходном документе. Значение по умолчанию — null, и префикс не добавляется в C++."
type: docs
weight: 4250
url: /ru/cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


Указывает префикс, который добавляется ко всем сгенерированным идентификаторам элементов в выходном документе. Значение по умолчанию — null, и префикс не добавляется.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## Примеры



Показывает, как добавить префикс, который добавляется ко всем сгенерированным идентификаторам элементов (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## См. также

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
