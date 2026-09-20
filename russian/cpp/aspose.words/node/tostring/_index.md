---
title: "Aspose::Words::Node::ToString method"
linktitle: "ToString"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Node::ToString method. Экспортирует содержимое узла в строку в указанном формате в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words/node/tostring/
---
## Node::ToString(Aspose::Words::SaveFormat) method


Экспортирует содержимое узла в строку в указанном формате.

```cpp
System::String Aspose::Words::Node::ToString(Aspose::Words::SaveFormat saveFormat)
```


### ReturnValue

Содержимое узла в указанном формате.

## Примеры



Показывает разницу между вызовами методов GetText и ToString для узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText получит видимый текст, а также коды полей и специальные символы.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString предоставит внешний вид документа, если сохранить его в указанный формат сохранения.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


Показывает, как извлечь метки списка из всех абзацев, являющихся элементами списка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Найдите, есть ли у нас список в абзаце. В нашем документе список использует обычные арабские цифры,
// которые начинаются с трёх и заканчиваются на шести.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // Это текст, который мы получаем при выводе этого узла в текстовый формат.
    // Этот вывод текста будет опускать метки списка. Удалите любые символы форматирования абзаца.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // Это получает позицию абзаца на текущем уровне списка. Если у нас есть список с несколькими уровнями,
    // это покажет, какую позицию он занимает на этом уровне.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // Объедините их, чтобы включить метку списка вместе с текстом в выводе.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```


Экспортирует содержимое узла в строку в формате HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// Когда мы вызываем метод ToString, используя перегрузку html SaveFormat,
// он преобразует содержимое узла в их необработанное представление html.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Мы также можем изменить результат этого преобразования, используя объект SaveOptions.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## См. также

* Enum [SaveFormat](../../saveformat/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Node::ToString(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Экспортирует содержимое узла в строку, используя указанные параметры сохранения.

```cpp
System::String Aspose::Words::Node::ToString(const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Указывает параметры, контролирующие способ сохранения узла. |

### ReturnValue

Содержимое узла в указанном формате.

## Примеры



Экспортирует содержимое узла в строку в формате HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// Когда мы вызываем метод ToString, используя перегрузку html SaveFormat,
// он преобразует содержимое узла в их необработанное представление html.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Мы также можем изменить результат этого преобразования, используя объект SaveOptions.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
