---
title: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout метод"
linktitle: "get_PreserveTableLayout"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout метод. Указывает, должна ли программа пытаться сохранять макет таблиц при сохранении в формате простого текста. Значение по умолчанию — false в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/txtsaveoptions/get_preservetablelayout/
---
## TxtSaveOptions::get_PreserveTableLayout method


Указывает, следует ли программе пытаться сохранять макет таблиц при сохранении в формат простого текста. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout() const
```


## Примеры



Показывает, как сохранять макет таблиц при конвертации в простой текст.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1");
builder->InsertCell();
builder->Write(u"Row 2, cell 2");
builder->EndTable();

// Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ сохранения документа в простой текст.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Установите свойство "PreserveTableLayout" в "true", чтобы применить заполнение пробелами к содержимому
// выходного документа простого текста, чтобы сохранить как можно больше макета таблицы.
// Установите свойство "PreserveTableLayout" в "false", чтобы сохранить содержимое всех таблиц
// как непрерывный блок текста, с одной новой строкой для каждой строки.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(System::String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") + u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
}
else
{
    ASSERT_EQ(System::String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## См. также

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
