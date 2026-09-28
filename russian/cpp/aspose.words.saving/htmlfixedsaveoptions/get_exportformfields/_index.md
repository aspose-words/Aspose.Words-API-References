---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields метод"
linktitle: "get_ExportFormFields"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields метод. Получает или задает указание, экспортируются ли поля формы как интерактивные элементы (как тег ''input'') вместо преобразования в текст или графику в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


Получает или задает индикатор того, экспортируются ли поля формы как интерактивные элементы (как тег 'input'), а не преобразуются в текст или графику.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## Примеры



Показывает, как экспортировать поля формы в Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// Когда мы экспортируем документ с полями формы в .html,
// существует два способа, которыми Aspose.Words может экспортировать поля формы.
// Установка флага "ExportFormFields" в "true" экспортирует их как интерактивные объекты.
// Установка этого флага в "false" отобразит поля формы как обычный текст.
// Это заморозит их в текущем значении и предотвратит возможность читателя нашего HTML‑документа
// взаимодействовать с ними.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportFormFields(exportFormFields);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")->get_Success());
}
```

## См. также

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
