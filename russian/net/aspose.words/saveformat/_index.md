---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.SaveFormat, чтобы легко выбирать форматы сохранения документов, улучшая управление файлами и совместимость для бесперебойных рабочих процессов.
type: docs
weight: 5580
url: /ru/net/aspose.words/saveformat/
---
## SaveFormat enumeration

Указывает формат, в котором сохранен документ.

```csharp
public enum SaveFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Unknown | `0` | Значение по умолчанию, недопустимое значение для формата файла. |
| Doc | `10` | Сохраняет документ в формате документа Microsoft Word 97 - 2007. |
| Dot | `11` | Сохраняет документ в формате шаблона Microsoft Word 97 - 2007. |
| Docx | `20` | Сохраняет документ как документ Office Open XML WordprocessingML (без макросов). |
| Docm | `21` | Сохраняет документ как документ Office Open XML WordprocessingML с поддержкой макросов. |
| Dotx | `22` | Сохраняет документ как шаблон Office Open XML WordprocessingML (без макросов). |
| Dotm | `23` | Сохраняет документ как шаблон Office Open XML WordprocessingML с поддержкой макросов. |
| FlatOpc | `24` | Сохраняет документ как Office Open XML WordprocessingML, хранящийся в плоском XML-файле вместо ZIP-пакета. |
| FlatOpcMacroEnabled | `25` | Сохраняет документ как документ Office Open XML WordprocessingML с поддержкой макросов, сохраненный в виде простого XML-файла вместо ZIP-архива. |
| FlatOpcTemplate | `26` | Сохраняет документ как шаблон Office Open XML WordprocessingML (без макросов), сохраненный в плоском XML-файле вместо ZIP-пакета. |
| FlatOpcTemplateMacroEnabled | `27` | Сохраняет документ как шаблон Office Open XML WordprocessingML с поддержкой макросов, сохраненный в плоском XML-файле вместо ZIP-пакета. |
| Rtf | `30` | Сохраняет документ в формате RTF. Все символы выше 7 бит экранируются как шестнадцатеричные или символы Unicode. |
| WordML | `31` | Сохраняет документ в формате Microsoft Word 2003 WordprocessingML. |
| Pdf | `40` | Сохраняет документ в формате PDF (Adobe Portable Document). |
| Xps | `41` | Сохраняет документ в формате XPS (XML Paper Specification). |
| XamlFixed | `42` | Сохраняет документ в формате Extensible Application Markup Language (XAML) как фиксированный документ. |
| Svg | `44` | Сохраняет документ в формате SVG (масштабируемая векторная графика). |
| HtmlFixed | `45` | Сохраняет документ в формате HTML с использованием абсолютно позиционированных элементов |
| OpenXps | `46` | Сохраняет документ в формате OpenXPS (Ecma-388). |
| Ps | `47` | Сохраняет документ в формате PS (PostScript). |
| Pcl | `48` | Сохраняет документ в формате PCL (Printer Control Language). |
| Html | `50` | Сохраняет документ в формате HTML. |
| Mhtml | `51` | Сохраняет документ в формате MHTML (веб-архив). |
| Epub | `52` | Сохраняет документ в формате EPUB. |
| Azw3 | `53` | Сохраняет документ в формате AZW3. |
| Mobi | `54` | Сохраняет документ в формате MOBI. |
| Odt | `60` | Сохраняет документ как текстовый документ ODF. |
| Ott | `61` | Сохраняет документ как шаблон текстового документа ODF. |
| Text | `70` | Сохраняет документ в формате простого текста. |
| XamlFlow | `71` | **Бета.** Сохраняет документ в формате XAML (Extensible Application Markup Language) как потоковый документ. |
| XamlFlowPack | `72` | **Бета.** Сохраняет документ в формате пакета Extensible Application Markup Language (XAML) как потоковый документ. |
| Markdown | `73` | Сохраняет документ в формате Markdown. |
| Xlsx | `80` | Сохраняет документ как документ Office Open XML SpreadsheetML (без макросов). |
| Tiff | `100` | Визуализирует страницу или страницы документа и сохраняет их в одностраничный или многостраничный файл TIFF. |
| Png | `101` | Отображает страницу документа и сохраняет ее как файл PNG. |
| Bmp | `102` | Отображает страницу документа и сохраняет ее как файл BMP. |
| Emf | `103` | Визуализирует страницу документа и сохраняет ее как векторный файл EMF (Enhanced Meta File). |
| Jpeg | `104` | Визуализирует страницу документа и сохраняет ее как файл JPEG. |
| Gif | `105` | Отображает страницу документа и сохраняет ее как файл GIF. |
| Eps | `106` | Визуализирует страницу документа и сохраняет ее как файл EPS. |
| WebP | `107` | Отображает страницу документа и сохраняет ее как файл WebP. |

## Примеры

Показывает, как конвертировать формат DOCX в HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Смотрите также

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
