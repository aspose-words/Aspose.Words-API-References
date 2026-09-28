---
title: "Метод Aspose::Words::ParagraphFormat::get_SpaceAfterAuto"
linktitle: "get_SpaceAfterAuto"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ParagraphFormat::get_SpaceAfterAuto. True, если величина отступа после абзаца задаётся автоматически в C++."
type: docs
weight: 32000
url: /ru/cpp/aspose.words/paragraphformat/get_spaceafterauto/
---
## ParagraphFormat::get_SpaceAfterAuto method


True, если величина интервала после абзаца задается автоматически.

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceAfterAuto()
```

## Примечания


Когда установлено в **true**, переопределяет действие [SpaceAfter](../get_spaceafter/).

Когда вы устанавливаете для абзаца Space Before и Space After значение Auto, **Microsoft** Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



## Примеры



Показывает, как установить автоматический интервал абзаца.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Примените большое количество отступов до и после абзацев, которые будет создавать этот построитель.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Установите эти флаги в "true", чтобы применить автоматический интервал,
// фактически игнорируя интервалы в свойствах, которые мы задали выше.
// Оставьте их как "false", и будет применён наш пользовательский интервал абзаца.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Вставьте два абзаца, у которых будет интервал сверху и снизу, и сохраните документ.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
