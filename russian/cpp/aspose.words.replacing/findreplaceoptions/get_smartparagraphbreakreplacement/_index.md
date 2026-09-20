---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement метод"
linktitle: "get_SmartParagraphBreakReplacement"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement метод. Получает или задает логическое значение, указывающее, разрешено ли заменять разрыв абзаца, когда нет следующего соседнего абзаца. Значение по умолчанию — false в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions::get_SmartParagraphBreakReplacement method


Получает или задает логическое значение, указывающее, разрешено ли заменять разрыв абзаца, когда нет следующего соседнего абзаца. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## Примеры



Показывает, как удалить абзац из ячейки таблицы с вложенной таблицей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте таблицу с абзацем и вложенной таблицей в первой ячейке.
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
// Когда следующая опция установлена в 'true', Aspose.Words удалит текст абзаца
// полностью вместе с его маркером абзаца. В противном случае Aspose.Words будет имитировать Word и удалит
// только текст абзаца, оставляя маркер абзаца нетронутым (когда после текста следует таблица).
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(get_ArtifactsDir() + u"Table.RemoveParagraphTextAndMark.docx");
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
