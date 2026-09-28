---
title: "Aspose::Words::Saving::CssSavingArgs::get_CssStream метод"
linktitle: "get_CssStream"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::CssSavingArgs::get_CssStream метод. Позволяет указать поток, в который будет сохраняться информация CSS в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


Позволяет указать поток, в который будет сохраняться информация CSS.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## Примечания


Это свойство позволяет сохранять информацию CSS в поток.

Значение по умолчанию — **null**. Это свойство не подавляет сохранение информации CSS в файл или встраивание в HTML‑документ. Чтобы подавить экспорт CSS, используйте свойство [IsExportNeeded](../get_isexportneeded/).

Используя [ICssSavingCallback](../../icsssavingcallback/), вы не можете заменить CSS другим. Он предназначен только для сохранения CSS в поток.

## См. также

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
