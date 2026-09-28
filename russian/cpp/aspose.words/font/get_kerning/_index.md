---
title: "Aspose::Words::Font::get_Kerning метод"
linktitle: "get_Kerning"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Font::get_Kerning метод. Получает или задает размер шрифта, при котором начинается кернинг в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


Получает или задаёт размер шрифта, с которого начинается кернинг.

```cpp
double Aspose::Words::Font::get_Kerning()
```


## Примеры



Показывает, как указать размер шрифта, при котором кернинг начинает действовать.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// Установите размер шрифта билдера и минимальный размер, при котором кернинг будет применяться.
// Размер шрифта опускается ниже порога кернинга, поэтому нижний фрагмент не будет иметь кернинг.
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// Установите порог кернинга так, чтобы текущий размер шрифта билдера был выше него.
// Любой текст, который мы добавляем с этой точки, будет иметь применённый кернинг. Пробелы между символами
// будут скорректированы, обычно в результате чего получаем слегка более эстетически приятный фрагмент текста.
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
