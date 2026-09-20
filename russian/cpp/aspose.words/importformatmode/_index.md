---
title: "Перечисление Aspose::Words::ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::ImportFormatMode. Указывает, как объединяется форматирование при импорте содержимого из другого документа в C++."
type: docs
weight: 93000
url: /ru/cpp/aspose.words/importformatmode/
---
## ImportFormatMode enum


Указывает, как объединяется форматирование при импорте содержимого из другого документа.

```cpp
enum class ImportFormatMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| UseDestinationStyles | 0 | Использовать стили целевого документа и копировать новые стили. Это вариант по умолчанию. |
| KeepSourceFormatting | 1 | Копировать все необходимые стили в целевой документ, при необходимости генерировать уникальные имена стилей. |
| KeepDifferentStyles | 2 | Копировать только стили, отличающиеся от стилей в исходном документе. |

## Примечания


Когда вы копируете узлы из одного документа в другой, эта опция определяет, как разрешается форматирование, если оба документа имеют стиль с одинаковым именем, но разным форматированием.

Форматирование разрешается следующим образом:

1. Встроенные стили сопоставляются с использованием их независимого от локали идентификатора стиля. Пользовательские стили сопоставляются с учётом регистра имени стиля.
1. Если соответствующий стиль не найден в целевом документе, стиль (и все стили, на которые он ссылается) копируются в целевой документ, и импортированные узлы обновляются, чтобы ссылаться на новый стиль.
1. Если соответствующий стиль уже существует в целевом документе, то то, что происходит, зависит от параметра **importFormatMode**, передаваемого в [ImportNode()](../), как описано ниже.



При использовании опции [UseDestinationStyles](./), если соответствующий стиль уже существует в целевом документе, стиль не копируется, и импортированные узлы обновляются, чтобы ссылаться на существующий стиль.

Недостаток использования [UseDestinationStyles](./) заключается в том, что импортированный текст может выглядеть иначе в целевом документе по сравнению с исходным документом. Например, стиль \"Heading 1\" в исходном документе использует шрифт Arial 16pt, а стиль \"Heading 1\" в целевом документе использует шрифт Times New Roman 14pt. При импорте текста стиля \"Heading 1\" без другого прямого форматирования он будет отображаться шрифтом Times New Roman 14pt в целевом документе.

[KeepSourceFormatting](./) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct [Node](../node/) attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct [Node](../node/) attributes in favor of preserving original [Node](../node/) formatting.

Недостаток использования [KeepSourceFormatting](./) состоит в том, что при выполнении нескольких импортов вы можете получить множество стилей в целевом документе, что может затруднить использование согласованного форматирования стилей в Microsoft Word для данного документа.

Использование опции [KeepDifferentStyles](./) позволяет переиспользовать стили целевого документа, если предоставляемое ими форматирование идентично стилям в исходном документе. Если стиль в целевом документе отличается от исходного, он импортируется.

## Примеры



Показывает, как вставить документ в другой документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
