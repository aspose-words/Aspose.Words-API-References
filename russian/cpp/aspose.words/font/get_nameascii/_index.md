---
title: "Aspose::Words::Font::get_NameAscii метод"
linktitle: "get_NameAscii"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Font::get_NameAscii метод. Возвращает или задаёт шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127) в C++."
type: docs
weight: 26000
url: /ru/cpp/aspose.words/font/get_nameascii/
---
## Font::get_NameAscii method


Возвращает или задаёт шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127).

```cpp
System::String Aspose::Words::Font::get_NameAscii()
```


## Примеры



Показывает, как Microsoft Word может комбинировать два разных шрифта в одном фрагменте.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Предположим фрагмент, который мы вставляем с помощью билдера, используя эту конфигурацию шрифта
// содержит символы в диапазоне ASCII. В этом случае,
// он будет отображать эти символы с использованием этого шрифта.
builder->get_Font()->set_NameAscii(u"Calibri");

// Если не указан другой шрифт, билдер также применит этот шрифт ко всем вставляемым символам.
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// Укажите шрифт для всех символов за пределами диапазона ASCII.
// Идеально, если у этого шрифта есть глиф для каждого требуемого не-ASCII кода символа.
builder->get_Font()->set_NameOther(u"Courier New");

// Вставьте фрагмент с одним словом, состоящим из ASCII‑символов, и одним словом, содержащим все символы за пределами этого диапазона.
// Каждый символ будет отображаться с использованием одного из шрифтов, в зависимости от.
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
