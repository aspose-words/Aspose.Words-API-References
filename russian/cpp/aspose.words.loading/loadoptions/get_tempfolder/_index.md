---
title: "метод Aspose::Words::Loading::LoadOptions::get_TempFolder"
linktitle: "get_TempFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Loading::LoadOptions::get_TempFolder. Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство имеет значение null и временные файлы не используются в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство равно **null**, и временные файлы не используются.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## Примечания


Папка должна существовать и быть доступной для записи, иначе будет выброшено исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения чтения.

## Примеры



Показывает, как загрузить документ, используя временные файлы.
```cpp
// Обратите внимание, что такой подход может снизить использование памяти, но ухудшает скорость.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// Убедитесь, что каталог существует, и загрузите
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);
```


Показывает, как использовать жесткий диск вместо памяти при загрузке документа.
```cpp
// При загрузке документа различные элементы временно сохраняются в памяти во время выполнения операции сохранения.
// Мы можем использовать эту опцию, чтобы вместо этого использовать временную папку в локальной файловой системе,
// что уменьшит нагрузку на память нашего приложения.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Указанная временная папка должна существовать в локальной файловой системе до операции загрузки.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", options);

// Папка будет сохраняться без остаточного содержимого после операции загрузки.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## См. также

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
