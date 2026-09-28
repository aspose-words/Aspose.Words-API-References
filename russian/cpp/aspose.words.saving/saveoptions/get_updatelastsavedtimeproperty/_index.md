---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty метод"
linktitle: "get_UpdateLastSavedTimeProperty"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty метод. Получает или задает значение, определяющее, обновляется ли свойство LastSavedTime перед сохранением в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


Получает или задает значение, определяющее, обновляется ли свойство [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) перед сохранением.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## Примеры



Показывает, как определить, следует ли сохранять свойство "Last saved time" документа при сохранении.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// Когда мы сохраняем документ в формат OOXML, мы можем создать объект OoxmlSaveOptions
// а затем передать его методу сохранения документа, чтобы изменить способ сохранения документа.
// Установите свойство "UpdateLastSavedTimeProperty" в "true", чтобы
// установить встроенное свойство "Last saved time" выходного документа в текущие дату/время.
// Установите свойство "UpdateLastSavedTimeProperty" в "false", чтобы
// сохранить исходное значение встроенного свойства "Last saved time" входного документа.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx");
System::DateTime lastSavedTimeNew = doc->get_BuiltInDocumentProperties()->get_LastSavedTime();

if (updateLastSavedTimeProperty)
{
    ASSERT_TRUE((System::DateTime::get_Now() - lastSavedTimeNew).get_Days() < 1);
}
else
{
    ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), lastSavedTimeNew);
}
```

## См. также

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
