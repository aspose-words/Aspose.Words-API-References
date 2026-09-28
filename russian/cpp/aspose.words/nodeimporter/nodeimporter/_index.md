---
title: "Aspose::Words::NodeImporter::NodeImporter конструктор"
linktitle: "NodeImporter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeImporter::NodeImporter конструктор. Инициализирует новый экземпляр класса NodeImporter в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) constructor


Инициализирует новый экземпляр класса [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Исходный документ. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Документ назначения, который будет владельцем импортированных узлов. |
| importFormatMode | Aspose::Words::ImportFormatMode | Указывает, как объединять конфликтующее форматирование стилей. |

## См. также

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) constructor


Инициализирует новый экземпляр класса [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Исходный документ. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Документ назначения, который будет владельцем импортированных узлов. |
| importFormatMode | Aspose::Words::ImportFormatMode | Указывает, как объединять конфликтующее форматирование стилей. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Указывает различные параметры для форматирования импортированного узла. |

## Примеры



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

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
