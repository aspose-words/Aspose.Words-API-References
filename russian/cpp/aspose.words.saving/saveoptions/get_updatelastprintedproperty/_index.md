---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty метод"
linktitle: "get_UpdateLastPrintedProperty"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty метод. Получает или задает значение, определяющее, обновляется ли свойство LastPrinted перед сохранением в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


Получает или задает значение, определяющее, обновляется ли свойство [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) перед сохранением.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## Примеры



Показывает, как обновить свойство документа "Last printed" при сохранении.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// Этот флаг определяет, обновляется ли дата последней печати, которая является встроенным свойством.
// Если да, то дата последней операции сохранения документа
// с переданным в качестве параметра объектом SaveOptions используется как дата печати.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// В Microsoft Word 2003 это свойство можно найти через Файл -> Свойства -> Статистика -> Печать.
// Оно также может быть отображено в теле документа с помощью поля PRINTDATE.
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Откройте сохранённый документ, затем проверьте значение свойства.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
{
    ASSERT_NE(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
else
{
    ASSERT_EQ(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
```

## См. также

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
