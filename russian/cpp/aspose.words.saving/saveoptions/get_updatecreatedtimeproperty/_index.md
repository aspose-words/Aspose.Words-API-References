---
title: "Метод Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty"
linktitle: "get_UpdateCreatedTimeProperty"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty. Получает или задает значение, определяющее, обновляется ли свойство CreatedTime перед сохранением. Значение по умолчанию — false; в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


Получает или задает значение, определяющее, обновляется ли свойство [CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) перед сохранением. Значение по умолчанию — **false**;.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## Примеры



Показывает, как обновить свойство "CreatedTime" документа при сохранении.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// Этот флаг определяет, обновляется ли время создания, которое является встроенным свойством.
// Если да, то дата последней операции сохранения документа
// при передаче этого объекта SaveOptions в качестве параметра используется в качестве времени создания.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Откройте сохранённый документ, затем проверьте значение свойства.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
{
    ASSERT_NE(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
else
{
    ASSERT_EQ(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
```

## См. также

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
