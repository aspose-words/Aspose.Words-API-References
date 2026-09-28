---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText метод"
linktitle: "get_ShowHiddenText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText метод. Получает или задает признак того, отображается ли скрытый текст в документе. По умолчанию false в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


Получает или задает индикатор того, отображается ли скрытый текст в документе. По умолчанию **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## Примеры



Показывает, как скрыть текст в отрендеренном выходном документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте скрытый текст, затем укажите, хотим ли мы опустить его в отрендеренном документе.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```

## См. также

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
