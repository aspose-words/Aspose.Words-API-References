---
title: "Aspose::Words::DocumentBase::get_PageColor метод"
linktitle: "get_PageColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBase::get_PageColor метод. Получает или задаёт цвет страницы документа. Это свойство является упрощённой версией BackgroundShape в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


Получает или задаёт цвет страницы документа. Это свойство — упрощённая версия [BackgroundShape](../get_backgroundshape/).

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## Примечания


Это свойство предоставляет простой способ указать сплошной цвет страницы для документа. Установка этого свойства создаёт и задаёт соответствующий [BackgroundShape](../get_backgroundshape/).

Если цвет страницы не установлен (например, в документе нет фоновой формы), возвращает **Empty**.

## Примеры



Показывает, как установить цвет фона для всех страниц документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(get_ArtifactsDir() + u"DocumentBase.SetPageColor.docx");
```

## См. также

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
