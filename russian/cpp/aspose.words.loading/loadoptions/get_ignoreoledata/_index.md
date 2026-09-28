---
title: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData метод"
linktitle: "get_IgnoreOleData"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData метод. Указывает, следует ли игнорировать данные OLE в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.loading/loadoptions/get_ignoreoledata/
---
## LoadOptions::get_IgnoreOleData method


Указывает, следует ли игнорировать данные OLE.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_IgnoreOleData() const
```

## Примечания


Игнорирование данных OLE может снизить потребление памяти и повысить производительность без потери данных в случае, когда целевой формат не поддерживает объекты OLE.

Значение по умолчанию — **false**.

## Примеры



Показывает, как игнорировать данные OLE при загрузке.
```cpp
// Игнорирование данных OLE может снизить потребление памяти и повысить производительность
// без потери данных в случае, когда целевой формат не поддерживает объекты OLE.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```

## См. также

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
