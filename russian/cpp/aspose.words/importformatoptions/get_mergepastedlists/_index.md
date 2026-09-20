---
title: "Метод Aspose::Words::ImportFormatOptions::get_MergePastedLists"
linktitle: "get_MergePastedLists"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ImportFormatOptions::get_MergePastedLists. Получает или задает логическое значение, указывающее, будут ли вставленные списки объединяться с окружающими списками. Значение по умолчанию — false в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


Получает или задает логическое значение, которое указывает, будут ли вставленные списки объединяться с окружающими списками. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## Примеры



Показывает, как объединять списки из документов.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// Установите свойство "MergePastedLists" в "true", и вставленные списки будут объединяться с окружающими списками.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```

## См. также

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
