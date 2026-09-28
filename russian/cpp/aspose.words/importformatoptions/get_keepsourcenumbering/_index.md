---
title: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering метод"
linktitle: "get_KeepSourceNumbering"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering метод. Получает или задает логическое значение, которое определяет, как нумерация будет импортирована, когда происходит конфликт в исходных и целевых документах. Значение по умолчанию — false в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/importformatoptions/get_keepsourcenumbering/
---
## ImportFormatOptions::get_KeepSourceNumbering method


Получает или задает логическое значение, которое определяет, как будет импортирована нумерация при конфликте в исходных и целевых документах. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering() const
```


## Примеры



Показывает, как импортировать документ с нумерованными списками.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

ASSERT_EQ(4, dstDoc->get_Lists()->get_Count());

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();

// Если происходит конфликт стилей списков, примените формат списка из исходного документа.
// Установите свойство "KeepSourceNumbering" в значение "false", чтобы не импортировать номера списков в целевой документ.
// Установите свойство "KeepSourceNumbering" в значение "true", чтобы импортировать все конфликтующие
// нумерацию стилей списков с тем же внешним видом, что и в исходном документе.
options->set_KeepSourceNumbering(isKeepSourceNumbering);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);
dstDoc->UpdateListLabels();

ASSERT_EQ(isKeepSourceNumbering ? 5 : 4, dstDoc->get_Lists()->get_Count());
```


Показывает, как решить конфликт при импорте документов, содержащих списки с одинаковым идентификатором определения списка.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// Установите свойство \"KeepSourceNumbering\" в значение \"true\", чтобы применить другой идентификатор определения списка
// к идентичным стилям, как Aspose.Words импортирует их в целевые документы.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


Показывает, как решить конфликты нумерации списков в исходных и целевых документах.
```cpp
// Откройте документ с пользовательской схемой нумерации списка, а затем клонируйте его.
// Поскольку оба имеют одинаковый формат нумерации, форматы столкнутся, если мы импортируем один документ в другой.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Когда мы импортируем клон документа в оригинал и затем добавляем его,
// тогда два списка с одинаковым форматом списка объединятся.
// Если мы установим флаг \"KeepSourceNumbering\" в значение \"false\", то список из клона документа
// который мы добавляем к оригиналу, продолжит нумерацию списка, к которому мы его добавляем.
// Это эффективно объединит два списка в один.
// Если мы установим флаг \"KeepSourceNumbering\" в значение \"true\", то клон документа
// список сохранит свою исходную нумерацию, и два списка будут выглядеть как отдельные списки.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(keepSourceNumbering);

auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, importFormatOptions);
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(srcDoc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    System::SharedPtr<Aspose::Words::Node> importedNode = importer->ImportNode(paragraph, true);
    dstDoc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Node>>(importedNode);
}

dstDoc->UpdateListLabels();

if (keepSourceNumbering)
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"6. Item 1\r\n" + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
else
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"10. Item 1\r\n" + u"11. Item 2 \r\n" + u"12. Item 3\r\n" + u"13. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
```

## См. также

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
