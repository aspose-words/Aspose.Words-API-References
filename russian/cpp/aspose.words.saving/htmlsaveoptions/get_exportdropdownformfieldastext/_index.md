---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText метод"
linktitle: "get_ExportDropDownFormFieldAsText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText method. Управляет тем, как выпадающие поля формы сохраняются в HTML или MHTML. Значение по умолчанию — false в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


Управляет тем, как выпадающие поля формы сохраняются в HTML или MHTML. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## Примечания


Когда установлено значение **true**, выпадающие поля формы экспортируются как обычный текст. Когда **false**, выпадающие поля формы экспортируются как элемент SELECT в HTML.

При экспорте в EPUB текстовые выпадающие поля формы всегда сохраняются как текст из‑за требований этого формата.

## Примеры



Показывает, как сделать так, чтобы выпадающие комбинированные поля формы сливались с текстом абзаца при сохранении в html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Используйте document builder, чтобы вставить комбинированный список со значением "Two", выбранным по умолчанию.
builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"One", u"Two", u"Three"}), 1);

// Флаг "ExportDropDownFormFieldAsText" этого объекта SaveOptions позволяет нам
// контролировать, как при сохранении документа в HTML обрабатываются выпадающие комбинированные списки.
// Установка значения "true" преобразует каждый комбинированный список в простой текст
// который отображает текущо выбранное значение списка, фактически фиксируя его.
// Установка значения "false" сохранит функциональность списка, используя теги <select> и <option>.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Two</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<select name=\"MyComboBox\">") + u"<option>One</option>" + u"<option selected=\"selected\">Two</option>" + u"<option>Three</option>" + u"</select>"));
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
