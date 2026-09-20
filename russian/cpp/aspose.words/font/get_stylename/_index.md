---
title: "Метод Aspose::Words::Font::get_StyleName"
linktitle: "get_StyleName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_StyleName. Получает или задает имя символьного стиля, применяемого к этому форматированию в C++."
type: docs
weight: 44000
url: /ru/cpp/aspose.words/font/get_stylename/
---
## Font::get_StyleName method


Получает или задает имя стиля символов, применяемого к этому форматированию.

```cpp
System::String Aspose::Words::Font::get_StyleName()
```


## Примеры



Показывает, как изменить стиль существующего текста.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два способа ссылки на стили.
// 1 -  Использование имени стиля:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  Использование встроенного идентификатора стиля:
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// Преобразовать все применения одного стиля в другой,
// используя вышеуказанные методы для ссылки на старые и новые стили.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == Aspose::Words::StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
