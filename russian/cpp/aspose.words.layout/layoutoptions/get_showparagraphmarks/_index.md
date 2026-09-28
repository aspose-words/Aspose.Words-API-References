---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks метод"
linktitle: "get_ShowParagraphMarks"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks метод. Получает или задает признак того, отображаются ли знаки абзаца. По умолчанию false в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.layout/layoutoptions/get_showparagraphmarks/
---
## LayoutOptions::get_ShowParagraphMarks method


Получает или задает индикатор того, отображаются ли знаки абзаца. По умолчанию **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks() const
```


## Примеры



Показывает, как отобразить знаки абзацев в отрендеренном выходном документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте несколько абзацев, затем включите отображение знаков абзацев, чтобы показать конец абзацев
// с символом абзацного знака (¶) при рендеринге документа.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```

## См. также

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
