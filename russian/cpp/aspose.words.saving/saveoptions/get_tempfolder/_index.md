---
title: "Aspose::Words::Saving::SaveOptions::get_TempFolder метод"
linktitle: "get_TempFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SaveOptions::get_TempFolder метод. Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство равно null и временные файлы не используются в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство равно **null**, и временные файлы не используются.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## Примечания


Когда Aspose.Words сохраняет документ, ему необходимо создать временные внутренние структуры. По умолчанию эти внутренние структуры создаются в памяти, и использование памяти резко возрастает на короткое время, пока документ сохраняется. После завершения сохранения память освобождается и собирается сборщиком мусора.

Указание временной папки с помощью [TempFolder](./) заставит Aspose.Words хранить внутренние структуры во временных файлах вместо памяти. Это уменьшает использование памяти во время сохранения, но снижает производительность сохранения.

Папка должна существовать и быть доступной для записи, иначе будет выброшено исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения сохранения.

## Примеры



Показывает, как использовать жёсткий диск вместо памяти при сохранении документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Когда мы сохраняем документ, различные элементы временно сохраняются в памяти во время выполнения операции сохранения.
// Мы можем использовать эту опцию, чтобы вместо этого использовать временную папку в локальной файловой системе,
// что уменьшит нагрузку на память нашего приложения.
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Указанная временная папка должна существовать в локальной файловой системе до начала операции сохранения.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// Папка будет сохраняться без остаточного содержимого после операции загрузки.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## См. также

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
