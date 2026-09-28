---
title: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions конструктор"
linktitle: "ChmLoadOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions конструктор. Инициализирует новый экземпляр этого класса со значениями по умолчанию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


Инициализирует новый экземпляр этого класса со значениями по умолчанию.

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


## Примеры



Показывает, как разрешать URL‑адреса вида "ms-its:myfile.chm::/index.htm".
```cpp
// Наш документ содержит URL-адреса, такие как "ms-its:amhelp.chm::....htm", но у него другое имя,
// поэтому ссылки на файлы не работают после сохранения в HTML.
// Нужно задать исходное имя файла в 'ChmLoadOptions', чтобы избежать этого поведения.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## См. также

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
