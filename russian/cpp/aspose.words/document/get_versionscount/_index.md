---
title: "Метод Aspose::Words::Document::get_VersionsCount"
linktitle: "get_VersionsCount"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_VersionsCount. Получает количество версий документа, хранящихся в DOC‑файле, на C++."
type: docs
weight: 57000
url: /ru/cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


Получает количество версий документа, сохранённых в DOC‑документе.

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## Примечания


Версии в Microsoft Word доступны через меню Файл/Версии. Microsoft Word поддерживает версии только для файлов DOC.

Это свойство позволяет определить, были ли версии документа, сохранённые в этом документе, до его открытия в Aspose.Words. Aspose.Words не предоставляет иной поддержки версий документов. Если сохранить этот документ с помощью Aspose.Words, он будет сохранён без версий.

## Примеры



Показывает, как работать с функцией подсчёта версий в более старых документах Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// Мы можем прочитать это свойство документа, но не можем сохранить его при сохранении.
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
