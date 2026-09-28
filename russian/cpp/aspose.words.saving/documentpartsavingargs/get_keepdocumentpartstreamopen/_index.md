---
title: "Метод Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen"
linktitle: "get_KeepDocumentPartStreamOpen"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen. Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения части документа в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/documentpartsavingargs/get_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method


Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения части документа.

```cpp
bool Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen() const
```

## Примечания


По умолчанию **false**, и Aspose.Words закроет поток, указанный в свойстве [DocumentPartStream](../get_documentpartstream/), после записи в него части документа. Укажите **true**, чтобы оставить поток открытым. Обратите внимание, что основной выходной поток, предоставленный при вызове [Save()](../) или [Save()](../), никогда не будет закрыт Aspose.Words, даже если [KeepDocumentPartStreamOpen](./) установлено в **false**.

## См. также

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
