---
title: "Метод Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor"
linktitle: "get_RevisedPropertiesColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor. Позволяет указать цвет, используемый для содержимого с изменениями свойств форматирования FormatChange. Значение по умолчанию — NoHighlight в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.layout/revisionoptions/get_revisedpropertiescolor/
---
## RevisionOptions::get_RevisedPropertiesColor method


Позволяет указать цвет, используемый для содержимого с изменениями свойств форматирования [FormatChange](../../../aspose.words/revisiontype/). Значение по умолчанию — [NoHighlight](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor()
```


## Примеры



Показывает, как изменить внешний вид правок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Получите объект RevisionOptions, который управляет внешним видом правок.
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> revisionOptions = doc->get_LayoutOptions()->get_RevisionOptions();

// Отображайте вставки правок зелёным цветом и курсивом.
revisionOptions->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::Green);
revisionOptions->set_InsertedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Italic);

// Отображайте удаления правок красным цветом и полужирным.
revisionOptions->set_DeletedTextColor(Aspose::Words::Layout::RevisionColor::Red);
revisionOptions->set_DeletedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Тот же текст появится дважды в правке перемещения:
// один раз в точке отправления и один раз в точке прибытия.
// Отображайте текст в правке перемещения из исходного места желтым с двойным зачёркиванием
// и двойным подчеркиванием синего цвета в правке перемещения в новое место.
revisionOptions->set_MovedFromTextColor(Aspose::Words::Layout::RevisionColor::Yellow);
revisionOptions->set_MovedFromTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleStrikeThrough);
revisionOptions->set_MovedToTextColor(Aspose::Words::Layout::RevisionColor::ClassicBlue);
revisionOptions->set_MovedToTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleUnderline);

// Отображайте правки формата тёмно-красным цветом и полужирным.
revisionOptions->set_RevisedPropertiesColor(Aspose::Words::Layout::RevisionColor::DarkRed);
revisionOptions->set_RevisedPropertiesEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Разместите толстую тёмно-синюю полосу слева от страницы рядом со строками, затронутыми правками.
revisionOptions->set_RevisionBarsColor(Aspose::Words::Layout::RevisionColor::DarkBlue);
revisionOptions->set_RevisionBarsWidth(15.0f);

// Покажите метки правок и оригинальный текст.
revisionOptions->set_ShowOriginalRevision(true);
revisionOptions->set_ShowRevisionMarks(true);

// Получите перемещения, удаления, правки форматирования и комментарии, отображаемые в зелёных баллонах
// на правой стороне страницы.
revisionOptions->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::Format);
revisionOptions->set_CommentColor(Aspose::Words::Layout::RevisionColor::BrightGreen);

// Эти функции применимы только к форматам, таким как .pdf или .jpg.
doc->Save(get_ArtifactsDir() + u"Revision.RevisionOptions.pdf");
```

## См. также

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
