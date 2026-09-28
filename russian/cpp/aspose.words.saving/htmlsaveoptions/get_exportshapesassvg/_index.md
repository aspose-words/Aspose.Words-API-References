---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg метод"
linktitle: "get_ExportShapesAsSvg"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg метод. Управляет тем, преобразуются ли узлы Shape в SVG‑изображения при сохранении в HTML, MHTML, EPUB или AZW3. Значение по умолчанию — false в C++."
type: docs
weight: 27000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions::get_ExportShapesAsSvg method


Управляет тем, преобразуются ли узлы [Shape](../../../aspose.words.drawing/shape/) в SVG‑изображения при сохранении в HTML, MHTML, EPUB или AZW3. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```

## Примечания


Если эта опция установлена в **true**, узлы [Shape](../../../aspose.words.drawing/shape/) экспортируются как элементы <svg>. В противном случае они рендерятся в растровые изображения и экспортируются как элементы <img>.

## Примеры



Показывает, как экспортировать фигуру в виде масштабируемой векторной графики.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// При сохранении документа в HTML мы можем передать объект SaveOptions
// для определения того, как операция сохранения будет экспортировать формы текстовых полей.
// Если установить флаг "ExportTextBoxAsSvg" в значение "true",
// операция сохранения преобразует фигуры с текстом в SVG‑объекты.
// Если установить флаг "ExportTextBoxAsSvg" в значение "false",
// операция сохранения преобразует фигуры с текстом в изображения.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportShapesAsSvg(exportShapesAsSvg);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height=\"80\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
