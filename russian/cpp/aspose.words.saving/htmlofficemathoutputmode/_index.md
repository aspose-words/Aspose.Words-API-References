---
title: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum. Указывает, как Aspose.Words экспортирует OfficeMath в HTML, MHTML и EPUB в C++."
type: docs
weight: 61000
url: /ru/cpp/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enum


Указывает, как Aspose.Words экспортирует OfficeMath в HTML, MHTML и EPUB.

```cpp
enum class HtmlOfficeMathOutputMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Image | 0 | OfficeMath преобразуется в HTML как изображение, указанное тегом <img>. |
| MathML | 1 | OfficeMath преобразуется в HTML с использованием MathML. |
| Text | 2 | OfficeMath преобразуется в HTML как последовательность фрагментов, указанных тегами <span>. |


## Примеры



Показано, как указать способ экспорта объектов Microsoft OfficeMath в HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

// При сохранении документа в HTML мы можем передать объект SaveOptions
// Определяет, как операция сохранения обрабатывает объекты OfficeMath.
// Установка свойства "OfficeMathOutputMode" в значение "HtmlOfficeMathOutputMode.Image"
// будет отображать каждый объект OfficeMath в виде изображения.
// Установка свойства "OfficeMathOutputMode" в значение "HtmlOfficeMathOutputMode.MathML"
// будет преобразовывать каждый объект OfficeMath в MathML.
// Установка свойства "OfficeMathOutputMode" в значение "HtmlOfficeMathOutputMode.Text"
// будет представлять каждую формулу OfficeMath в виде обычного HTML‑текста.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_OfficeMathOutputMode(htmlOfficeMathOutputMode);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.OfficeMathOutputMode.html", options);
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::Image:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\"margin-top:0pt; margin-bottom:10pt\">") + u"<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"163\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " + u"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::MathML:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">") + u"<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" + u"<mi>i</mi>" + u"<mo>[+]</mo>" + u"<mi>b</mi>" + u"<mo>-</mo>" + u"<mi>c</mi>" + u"<mo>≥</mo>" + u".*" + u"</math>" + u"</p>")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::Text:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\\\"margin-top:0pt; margin-bottom:10pt; text-align:center\\\">") + u"<span style=\\\"font-family:'Cambria Math'\\\">i[+]b-c≥iM[+]bM-cM </span>" + u"</p>")->get_Success());
        break;

}
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
