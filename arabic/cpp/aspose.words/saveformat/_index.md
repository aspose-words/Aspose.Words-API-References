---
title: "Aspose::Words::SaveFormat enum"
linktitle: "SaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::SaveFormat enum. يشير إلى التنسيق الذي يُحفظ به المستند في C++."
type: docs
weight: 114000
url: /ar/cpp/aspose.words/saveformat/
---
## SaveFormat enum


يشير إلى الصيغة التي يُحفظ بها المستند.

```cpp
enum class SaveFormat
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| غير معروف | 0 | الافتراضي، قيمة غير صالحة لتنسيق الملف. |
| Doc | 10 | يحفظ المستند بتنسيق Microsoft Word 97 - 2007 [Document](../document/). |
| Dot | 11 | يحفظ المستند بتنسيق قالب Microsoft Word 97 - 2007. |
| Docx | 20 | يحفظ المستند كـ [Document](../document/) من نوع Office Open XML WordprocessingML (بدون ماكرو). |
| Docm | 21 | يحفظ المستند كـ [Document](../document/) من نوع Office Open XML WordprocessingML مع تمكين الماكرو. |
| Dotx | 22 | يحفظ المستند كقالب Office Open XML WordprocessingML (بدون ماكرو). |
| Dotm | 23 | يحفظ المستند كقالب Office Open XML WordprocessingML مع تمكين الماكرو. |
| FlatOpc | 24 | يحفظ المستند كـ Office Open XML WordprocessingML مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcMacroEnabled | 25 | يحفظ المستند كـ [Document](../document/) من نوع Office Open XML WordprocessingML مع تمكين الماكرو مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplate | 26 | يحفظ المستند كقالب Office Open XML WordprocessingML (بدون ماكرو) مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplateMacroEnabled | 27 | يحفظ المستند كقالب Office Open XML WordprocessingML مع تمكين الماكرو مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| Rtf | 30 | يحفظ المستند بتنسيق RTF. جميع الأحرف التي تتجاوز 7 بتات يتم هروبها كقيمة سداسية عشرية أو أحرف يونيكود. |
| WordML | 31 | يحفظ المستند بتنسيق Microsoft Word 2003 WordprocessingML. |
| Pdf | 40 | يحفظ المستند بتنسيق PDF (Adobe Portable [Document](../document/)). |
| Xps | 41 | يحفظ المستند بتنسيق XPS (XML Paper Specification). |
| XamlFixed | 42 | يحفظ المستند بتنسيق لغة Extensible Application [Markup](../../aspose.words.markup/) (XAML) كمستند ثابت. |
| Svg | 44 | يحفظ المستند بتنسيق Svg (Scalable Vector Graphics). |
| HtmlFixed | 45 | يحفظ المستند بتنسيق HTML باستخدام عناصر موضوعة بشكل مطلق. |
| OpenXps | 46 | يحفظ المستند بتنسيق OpenXPS (Ecma-388). |
| Ps | 47 | يحفظ المستند بتنسيق PS (PostScript). |
| Pcl | 48 | يحفظ المستند بتنسيق PCL (Printer Control Language). |
| Html | 50 | يحفظ المستند بتنسيق HTML. |
| Mhtml | 51 | يحفظ المستند بتنسيق MHTML (Web archive). |
| Epub | 52 | يحفظ المستند بتنسيق EPUB. |
| Azw3 | 53 | يحفظ المستند بتنسيق AZW3. |
| Mobi | 54 | يحفظ المستند بتنسيق MOBI. |
| Odt | 60 | يحفظ المستند كـ ODF Text [Document](../document/). |
| Ott | 61 | يحفظ المستند كقالب ODF Text [Document](../document/). |
| Text | 70 | يحفظ المستند بتنسيق نص عادي. |
| XamlFlow | 71 | **Beta.** يحفظ المستند بتنسيق لغة Extensible Application [Markup](../../aspose.words.markup/) (XAML) كمستند تدفق. |
| XamlFlowPack | 72 | **Beta.** يحفظ المستند بتنسيق حزمة لغة Extensible Application [Markup](../../aspose.words.markup/) (XAML) كمستند تدفق. |
| Markdown | 73 | يحفظ المستند بتنسيق Markdown. |
| Xlsx | 80 | يحفظ المستند كـ Office Open XML SpreadsheetML [Document](../document/) (بدون ماكرو). |
| Docling | 81 | يحفظ المستند بتنسيق Docling JSON. |
| Tiff | 100 | يقوم بتصيير صفحة أو صفحات من المستند ويحفظها في ملف TIFF واحد أو متعدد الصفحات. |
| Png | 101 | يقوم بتصيير صفحة من المستند ويحفظها كملف PNG. |
| Bmp | 102 | يقوم بتصيير صفحة من المستند ويحفظها كملف BMP. |
| Emf | 103 | يقوم بتصيير صفحة من المستند ويحفظها كملف EMF متجه (Enhanced Meta File). |
| Jpeg | 104 | يقوم بتصيير صفحة من المستند ويحفظها كملف JPEG. |
| Gif | 105 | يقوم بتصيير صفحة من المستند ويحفظها كملف GIF. |
| Eps | 106 | يقوم بتصيير صفحة من المستند ويحفظها كملف EPS. |


## أمثلة



يظهر كيفية التحويل من تنسيق DOCX إلى HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
