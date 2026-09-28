---
title: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins"
linktitle: "get_ExportPageMargins"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins. Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. По умолчанию — false в C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. По умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## Примеры



Показывает, как отображать объекты за пределами границ в выводимых HTML‑документах.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Используйте построитель для вставки фигуры без обтекания.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Отрицательные значения позиции фигуры могут разместить её за пределами границ страницы.
// Если экспортировать это в HTML, фигура будет обрезана.
shape->set_Left(-150);

// При сохранении документа в HTML мы можем передать объект SaveOptions
// чтобы решить, следует ли корректировать страницу для полного отображения объектов за пределами границ.
// Если установить флаг "ExportPageMargins" в значение "true", фигура будет полностью видна в выводимом HTML.
// Если установить флаг "ExportPageMargins" в значение "false",
// наш документ отобразит фигуру обрезанной, как это происходит в Microsoft Word.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
