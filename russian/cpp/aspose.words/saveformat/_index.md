---
title: "Aspose::Words::SaveFormat enum"
linktitle: "SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::SaveFormat enum. Указывает формат, в котором документ сохраняется в C++."
type: docs
weight: 114000
url: /ru/cpp/aspose.words/saveformat/
---
## SaveFormat enum


Указывает формат, в котором сохраняется документ.

```cpp
enum class SaveFormat
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Неизвестно | 0 | По умолчанию, недопустимое значение формата файла. |
| Doc | 10 | Сохраняет документ в формате Microsoft Word 97‑2007 [Document](../document/). |
| Dot | 11 | Сохраняет документ в формате шаблона Microsoft Word 97‑2007. |
| Docx | 20 | Сохраняет документ как Office Open XML WordprocessingML [Document](../document/) (без макросов). |
| Docm | 21 | Сохраняет документ как Office Open XML WordprocessingML с поддержкой макросов [Document](../document/). |
| Dotx | 22 | Сохраняет документ как шаблон Office Open XML WordprocessingML (без макросов). |
| Dotm | 23 | Сохраняет документ как шаблон Office Open XML WordprocessingML с поддержкой макросов. |
| FlatOpc | 24 | Сохраняет документ как Office Open XML WordprocessingML, хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| FlatOpcMacroEnabled | 25 | Сохраняет документ как Office Open XML WordprocessingML с поддержкой макросов [Document](../document/), хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| FlatOpcTemplate | 26 | Сохраняет документ как шаблон Office Open XML WordprocessingML (без макросов), хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| FlatOpcTemplateMacroEnabled | 27 | Сохраняет документ как шаблон Office Open XML WordprocessingML с поддержкой макросов, хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| Rtf | 30 | Сохраняет документ в формате RTF. Все символы выше 7‑бит экранируются в виде шестнадцатеричных или Unicode‑символов. |
| WordML | 31 | Сохраняет документ в формате Microsoft Word 2003 WordprocessingML. |
| Pdf | 40 | Сохраняет документ в формате PDF (Adobe Portable [Document](../document/)). |
| Xps | 41 | Сохраняет документ в формате XPS (XML Paper Specification). |
| XamlFixed | 42 | Сохраняет документ в формате Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) как фиксированный документ. |
| Svg | 44 | Сохраняет документ в формате Svg (Scalable Vector Graphics). |
| HtmlFixed | 45 | Сохраняет документ в формате HTML, используя абсолютно позиционированные элементы. |
| OpenXps | 46 | Сохраняет документ в формате OpenXPS (Ecma-388). |
| Ps | 47 | Сохраняет документ в формате PS (PostScript). |
| Pcl | 48 | Сохраняет документ в формате PCL (Printer Control Language). |
| Html | 50 | Сохраняет документ в формате HTML. |
| Mhtml | 51 | Сохраняет документ в формате MHTML (Web archive). |
| Epub | 52 | Сохраняет документ в формате EPUB. |
| Azw3 | 53 | Сохраняет документ в формате AZW3. |
| Mobi | 54 | Сохраняет документ в формате MOBI. |
| Odt | 60 | Сохраняет документ как ODF Text [Document](../document/). |
| Ott | 61 | Сохраняет документ как шаблон ODF Text [Document](../document/). |
| Text | 70 | Сохраняет документ в простом текстовом формате. |
| XamlFlow | 71 | **Beta.** Сохраняет документ в формате Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) как потоковый документ. |
| XamlFlowPack | 72 | **Beta.** Сохраняет документ в формате пакета Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) как потоковый документ. |
| Markdown | 73 | Сохраняет документ в формате Markdown. |
| Xlsx | 80 | Сохраняет документ как Office Open XML SpreadsheetML [Document](../document/) (без макросов). |
| Docling | 81 | Сохраняет документ в формате Docling JSON. |
| Tiff | 100 | Отрисовывает одну или несколько страниц документа и сохраняет их в один или многостраничный файл TIFF. |
| Png | 101 | Отрисовывает страницу документа и сохраняет её как файл PNG. |
| Bmp | 102 | Отрисовывает страницу документа и сохраняет её как файл BMP. |
| Emf | 103 | Отрисовывает страницу документа и сохраняет её как векторный файл EMF (Enhanced Meta File). |
| Jpeg | 104 | Отрисовывает страницу документа и сохраняет её как файл JPEG. |
| Gif | 105 | Отрисовывает страницу документа и сохраняет её как файл GIF. |
| Eps | 106 | Отрисовывает страницу документа и сохраняет её как файл EPS. |


## Примеры



Показывает, как преобразовать DOCX в формат HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
