---
title: "Метод Aspose::Words::Font::get_Bidi"
linktitle: "get_Bidi"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Bidi. Указывает, будет ли содержимое этого фрагмента иметь характеристики справа налево в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/font/get_bidi/
---
## Font::get_Bidi method


Указывает, должны ли содержимое этого фрагмента иметь свойства справа налево.

```cpp
bool Aspose::Words::Font::get_Bidi()
```

## Примечания


Это свойство, когда включено, не должно использоваться с явно левосторонним текстом. Любое поведение в этом случае не определено. Это свойство, когда отключено, не должно использоваться с явно правосторонним текстом. Любое поведение в этом случае не определено.

Когда содержимое этого фрагмента отображается, все символы должны рассматриваться как символы сложных скриптов для целей форматирования. Это означает, что [BoldBi](../get_boldbi/), [ItalicBi](../get_italicbi/), [SizeBi](../get_sizebi/) и соответствующее имя шрифта будут использоваться при рендеринге этого фрагмента.

Кроме того, когда содержимое этого фрагмента отображается, это свойство действует как переопределение справа налево для символов, классифицированных как "слабые типы" и "нейтральные типы".

## Примеры



Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста справа налево.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Определите набор параметров шрифта для текста слева направо.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Определите другой набор параметров шрифта для текста справа налево.
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// Мы можем использовать флаг Bidi, чтобы указать, является ли добавляемый текст
// в документе, создаваемом DocumentBuilder, справа налево. Когда мы добавляем текст с этим флагом, установленным в true,
// он будет отформатирован с использованием набора параметров шрифта для текста справа налево.
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// Установите флаг в false, а затем добавьте текст слева направо.
// DocumentBuilder отформатирует их, используя набор параметров шрифта для текста слева направо.
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
