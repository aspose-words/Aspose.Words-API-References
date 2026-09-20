---
title: "Aspose::Words::NodeImporter class"
linktitle: "NodeImporter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeImporter class. Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 44000
url: /ru/cpp/aspose.words/nodeimporter/
---
## NodeImporter class


Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой. Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeImporter : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Импортирует узел из одного документа в другой. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | Инициализирует новый экземпляр класса [NodeImporter](./). |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Инициализирует новый экземпляр класса [NodeImporter](./). |
| static [Type](./type/)() |  |
## Примечания


Aspose.Words предоставляет функциональность для простого копирования и перемещения фрагментов между документами Microsoft Word. Это известно как "importing nodes". Прежде чем вы сможете вставить фрагмент из одного документа в другой, его необходимо "import". Импорт создает глубокую копию оригинального узла, готовую к вставке в целевой документ.

Самый простой способ импортировать узел — использовать метод [ImportNode()](../), предоставляемый объектом [DocumentBase](../documentbase/).

Однако, когда вам необходимо импортировать узлы из одного документа в другой многократно, лучше использовать класс [NodeImporter](./). Класс [NodeImporter](./) позволяет минимизировать количество стилей и списков, создаваемых в целевом документе.

Копирование или перемещение фрагментов из одного документа Microsoft Word в другой представляет ряд технических проблем для Aspose.Words. В документе Word стили и форматирование списков хранятся централизованно, отдельно от текста документа. Абзацы и последовательности текста лишь ссылаются на стили по внутренним уникальным идентификаторам.

Проблемы возникают из‑за того, что стили и списки различаются в разных документах. Например, чтобы скопировать абзац, отформатированный стилем Heading 1, из одного документа в другой, необходимо учитывать несколько факторов: решить, копировать ли стиль Heading 1 из исходного документа в целевой, клонировать абзац, обновить клонированный абзац так, чтобы он ссылался на правильный стиль Heading 1 в целевом документе. Если стиль необходимо скопировать, следует проанализировать и, возможно, скопировать все стили, на которые он ссылается (на основе стиля и стиля следующего абзаца), и так далее. Аналогичные проблемы возникают при копировании маркированных или нумерованных абзацев, поскольку Microsoft Word хранит определения списков отдельно от текста.

Класс [NodeImporter](./) похож на контекст, который хранит "translation tables" во время импорта. Он корректно преобразует стили и списки между исходным и целевым документами.

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
