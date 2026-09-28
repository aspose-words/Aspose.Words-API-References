---
title: "Aspose::Words::Document::get_LayoutOptions метод"
linktitle: "get_LayoutOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::get_LayoutOptions метод. Получает объект LayoutOptions, который представляет параметры управления процессом разметки этого документа на C++."
type: docs
weight: 36000
url: /ru/cpp/aspose.words/document/get_layoutoptions/
---
## Document::get_LayoutOptions method


Получает объект [LayoutOptions](../../../aspose.words.layout/layoutoptions/), который представляет параметры управления процессом разметки этого документа.

```cpp
System::SharedPtr<Aspose::Words::Layout::LayoutOptions> Aspose::Words::Document::get_LayoutOptions() const
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


Показывает, как изменить внешний вид правок в отрендеренном выходном документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте правку, затем измените цвет всех правок на зелёный.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Удалите полосу, которая появляется слева от каждой исправленной строки.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## См. также

* Class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
