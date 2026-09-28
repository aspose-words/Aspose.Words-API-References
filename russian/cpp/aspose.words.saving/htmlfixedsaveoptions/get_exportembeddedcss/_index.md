---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss метод"
linktitle: "get_ExportEmbeddedCss"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss метод. Указывает, должен ли CSS (Cascading Style Sheet) быть встроен в документ Html в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedCss method


Указывает, должен ли CSS (Cascading [Style](../../../aspose.words/style/) Sheet) быть встроен в документ Html.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## Примеры



Показывает, как определить, где хранить таблицы стилей CSS при экспорте документа в Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Когда мы экспортируем документ в html, Aspose.Words также создаст таблицу стилей CSS для форматирования документа.
// Установка флага "ExportEmbeddedCss" в значение "true" сохраняет таблицу стилей CSS в файл .css,
// и связывает файл с html‑документом с помощью элемента <link>.
// Установка флага в значение "false" встроит таблицу стилей CSS в документ Html,
// что создаст только один файл вместо двух.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedCss(exportEmbeddedCss);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<style type=\"text/css\">")->get_Success());
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />")->get_Success());
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

## См. также

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
