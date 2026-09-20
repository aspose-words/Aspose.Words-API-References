---
title: "Метод Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName"
linktitle: "get_OriginalFileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName. Имя файла CHM. Значение по умолчанию — null в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


Имя CHM‑файла. Значение по умолчанию — **null**.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## Примечания


Документы CHM могут содержать ссылки, которые ссылаются на тот же документ по имени файла. Aspose.Words поддерживает такие ссылки и обычно использует [OriginalFileName](../../../aspose.words/document/get_originalfilename/) для проверки, является ли файл, на который указывает ссылка, загружаемым файлом. Если документ загружается из потока, его оригинальное имя файла должно быть указано явно через это свойство, поскольку оно не может быть определено автоматически.

Если документ CHM загружается из файла и для этого свойства указано ненулевое значение, оно будет иметь приоритет над фактическим именем файла, хранящимся в [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

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
