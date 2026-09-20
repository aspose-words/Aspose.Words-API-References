---
title: "Aspose::Words::Font::get_NoProofing метод"
linktitle: "get_NoProofing"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Font::get_NoProofing метод. True, когда отформатированные символы не проверяются орфографией в C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


Истина, когда отформатированные символы не подлежат проверке орфографии.

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## Примеры



Показывает, как предотвратить проверку орфографии текста в Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Обычно Microsoft Word подчеркивает орфографические ошибки неровным красным подчеркиванием.
// Мы можем снять флаг "NoProofing", чтобы создать часть текста, которая
// обходит проверку орфографии, полностью её отключая.
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(get_ArtifactsDir() + u"Font.NoProofing.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
