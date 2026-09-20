---
title: "Метод Aspose::Words::Font::get_ComplexScript"
linktitle: "get_ComplexScript"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_ComplexScript. Указывает, следует ли рассматривать содержимое этого пробега как текст сложного сценария независимо от их значений Unicode при определении форматирования этого пробега в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/font/get_complexscript/
---
## Font::get_ComplexScript method


Указывает, следует ли рассматривать содержимое этого фрагмента как текст сложного сценария независимо от их значений Unicode при определении форматирования этого фрагмента.

```cpp
bool Aspose::Words::Font::get_ComplexScript()
```


## Примеры



Показывает, как добавить текст, который всегда рассматривается как текст сложного сценария.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
