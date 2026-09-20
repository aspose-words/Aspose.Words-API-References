---
title: "Метод Aspose::Words::Font::get_Hidden"
linktitle: "get_Hidden"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Hidden. Возвращает true, если шрифт отформатирован как скрытый текст в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


Истина, если шрифт отформатирован как скрытый текст.

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## Примеры



Показывает, как создать фрагмент скрытого текста.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Если флаг Hidden установлен в true, любой текст, созданный с помощью этого объекта Font, будет невидим в документе.
// Мы не увидим и не выделим скрытый текст, пока не включим параметр "Hidden text".
// находится в Microsoft Word через "File" -> "Options" -> "Display". Текст всё равно будет присутствовать,
// и мы сможем получить доступ к этому тексту программно.
// Не рекомендуется использовать этот метод для скрытия конфиденциальной информации.
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
