---
title: "Aspose::Words::ImportFormatOptions класс"
linktitle: "ImportFormatOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ImportFormatOptions класс. Позволяет задавать различные параметры импорта для форматирования вывода. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 35000
url: /ru/cpp/aspose.words/importformatoptions/
---
## ImportFormatOptions class


Позволяет указать различные параметры импорта для форматирования вывода. Чтобы узнать больше, посетите статью документации [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class ImportFormatOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/)() const | Получает или задает логическое значение, которое указывает, следует ли автоматически регулировать интервалы между предложениями и словами. Значение по умолчанию — **false**. |
| [get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/)() const | Получает или задает логическое значение, указывающее, следует ли принудительно изменить тип первой импортированной секции на [NewPage](../sectionstart/) при вызове [AppendDocument()](../). Значение по умолчанию — **true**. |
| [get_ForceCopyStyles](./get_forcecopystyles/)() const | Получает или задает логическое значение, указывающее, копировать ли конфликтующие стили в режиме [KeepSourceFormatting](../importformatmode/). Значение по умолчанию — **false**. |
| [get_IgnoreHeaderFooter](./get_ignoreheaderfooter/)() const | Получает или задает логическое значение, которое указывает, что исходное форматирование содержимого верхних/нижних колонтитулов игнорируется, если используется режим [KeepSourceFormatting](../importformatmode/). Значение по умолчанию — **true**. |
| [get_IgnoreTextBoxes](./get_ignoretextboxes/)() const | Получает или задает логическое значение, которое указывает, что исходное форматирование содержимого текстовых полей игнорируется, если используется режим [KeepSourceFormatting](../importformatmode/). Значение по умолчанию — **true**. |
| [get_KeepSourceNumbering](./get_keepsourcenumbering/)() const | Получает или задает логическое значение, которое определяет, как будет импортирована нумерация при конфликте в исходных и целевых документах. Значение по умолчанию — **false**. |
| [get_MergePastedLists](./get_mergepastedlists/)() const | Получает или задает логическое значение, которое указывает, будут ли вставленные списки объединяться с окружающими списками. Значение по умолчанию — **false**. |
| [get_ResolveThemeColors](./get_resolvethemecolors/)() const | Получает или задает логическое значение, которое указывает, следует ли принудительно разрешать темы цветов фигур. Значение по умолчанию — **false**. |
| [get_SmartStyleBehavior](./get_smartstylebehavior/)() const | Получает или задает логическое значение, которое определяет, как стили будут импортированы, когда они имеют одинаковые имена в исходных и целевых документах. Значение по умолчанию — **false**. |
| [GetType](./gettype/)() const override |  |
| [ImportFormatOptions](./importformatoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AdjustSentenceAndWordSpacing](./set_adjustsentenceandwordspacing/)(bool) | Сеттер для [Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/). |
| [set_AppendDocumentWithNewPage](./set_appenddocumentwithnewpage/)(bool) | Сеттер для [Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/). |
| [set_ForceCopyStyles](./set_forcecopystyles/)(bool) | Сеттер для [Aspose::Words::ImportFormatOptions::get_ForceCopyStyles](./get_forcecopystyles/). |
| [set_IgnoreHeaderFooter](./set_ignoreheaderfooter/)(bool) | Сеттер для [Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter](./get_ignoreheaderfooter/). |
| [set_IgnoreTextBoxes](./set_ignoretextboxes/)(bool) | Сеттер для [Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes](./get_ignoretextboxes/). |
| [set_KeepSourceNumbering](./set_keepsourcenumbering/)(bool) | Сеттер для [Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering](./get_keepsourcenumbering/). |
| [set_MergePastedLists](./set_mergepastedlists/)(bool) | Сеттер для [Aspose::Words::ImportFormatOptions::get_MergePastedLists](./get_mergepastedlists/). |
| [set_ResolveThemeColors](./set_resolvethemecolors/)(bool) | Сеттер для [Aspose::Words::ImportFormatOptions::get_ResolveThemeColors](./get_resolvethemecolors/). |
| [set_SmartStyleBehavior](./set_smartstylebehavior/)(bool) | Сеттер для [Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior](./get_smartstylebehavior/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как разрешать дублирующиеся стили при вставке документов.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Клонируйте документ и отредактируйте стиль "MyStyle" клона, чтобы он имел другой цвет, чем у оригинала.
// Если вставить клон в оригинальный документ, два стиля с одинаковым именем вызовут конфликт.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Когда мы включаем SmartStyleBehavior и используем режим импорта KeepSourceFormatting,
// Aspose.Words разрешит конфликты стилей, преобразуя стили исходного документа.
// с теми же именами, что и стили назначения, в прямые атрибуты абзаца.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
