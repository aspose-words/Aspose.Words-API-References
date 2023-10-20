---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: Aspose.Words.SaveFormat تعداد. يشير إلى التنسيق الذي يتم حفظ المستند به في C#.
type: docs
weight: 4840
url: /ar/net/aspose.words/saveformat/
---
## SaveFormat enumeration

يشير إلى التنسيق الذي يتم حفظ المستند به.

```csharp
public enum SaveFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Unknown | `0` | القيمة الافتراضية، غير صالحة لتنسيق الملف. |
| Doc | `10` | يحفظ المستند بتنسيق مستند Microsoft Word 97 - 2007. |
| Dot | `11` | يحفظ المستند بتنسيق قالب Microsoft Word 97 - 2007. |
| Docx | `20` | يحفظ المستند كمستند Office Open XML WordprocessingML (خالي من وحدات الماكرو). |
| Docm | `21` | يحفظ المستند كمستند Office Open XML WordprocessingML الممكّن بماكرو. |
| Dotx | `22` | يحفظ المستند كقالب Office Open XML WordprocessingML (خالي من وحدات الماكرو). |
| Dotm | `23` | يحفظ المستند كقالب ممكن بماكرو لـ Office Open XML WordprocessingML. |
| FlatOpc | `24` | يحفظ المستند كملف Office Open XML WordprocessingML المخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcMacroEnabled | `25` | يحفظ المستند كمستند Office Open XML WordprocessingML الممكّن بماكرو والمخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplate | `26` | يحفظ المستند كقالب Office Open XML WordprocessingML (خالي من وحدات الماكرو) المخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | يحفظ المستند كقالب تمكين ماكرو لـ Office Open XML WordprocessingML مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| Rtf | `30` | يحفظ المستند بتنسيق RTF. يتم تخطي كافة الأحرف التي يزيد طولها عن 7 بت كأحرف سداسية عشرية أو Unicode. |
| WordML | `31` | يحفظ المستند بتنسيق Microsoft Word 2003 WordprocessingML. |
| Pdf | `40` | يحفظ المستند بتنسيق PDF (Adobe Portable Document). |
| Xps | `41` | يحفظ المستند بتنسيق XPS (مواصفات ورق XML). |
| XamlFixed | `42` | يحفظ المستند بتنسيق لغة توصيف التطبيقات القابلة للتوسيع (XAML) كمستند ثابت. |
| Svg | `44` | يحفظ المستند بتنسيق Svg (رسومات متجهة قابلة للتحجيم). |
| HtmlFixed | `45` | يحفظ المستند بتنسيق HTML باستخدام عناصر ذات موضع مطلق |
| OpenXps | `46` | يحفظ المستند بتنسيق OpenXPS (Ecma-388). |
| Ps | `47` | يحفظ المستند بتنسيق PS (PostScript). |
| Pcl | `48` | يحفظ المستند بتنسيق PCL (لغة التحكم في الطابعة). |
| Html | `50` | يحفظ المستند بتنسيق HTML. |
| Mhtml | `51` | يحفظ المستند بتنسيق MHTML (أرشيف الويب). |
| Epub | `52` | يحفظ المستند بتنسيق EPUB. |
| Azw3 | `53` | يحفظ المستند بتنسيق AZW3. |
| Mobi | `54` | يحفظ المستند بتنسيق MOBI. |
| Odt | `60` | يحفظ المستند كمستند نصي ODF. |
| Ott | `61` | يحفظ المستند كقالب مستند نصي ODF. |
| Text | `70` | يحفظ المستند بتنسيق النص العادي. |
| XamlFlow | `71` | **بيتا.** يحفظ المستند بتنسيق لغة توصيف التطبيقات القابلة للتوسيع (XAML) كمستند تدفق. |
| XamlFlowPack | `72` | **بيتا.** يحفظ المستند بتنسيق حزمة لغة توصيف التطبيقات القابلة للتوسيع (XAML) كمستند تدفق. |
| Markdown | `73` | يحفظ المستند بتنسيق Markdown. |
| Xlsx | `80` | يحفظ المستند كمستند Office Open XML SpreadsheetML (خالي من وحدات الماكرو). |
| Tiff | `100` | يعرض صفحة أو صفحات من المستند ويحفظها في ملف TIFF فردي أو متعدد الصفحات. |
| Png | `101` | يعرض صفحة من المستند ويحفظها كملف PNG. |
| Bmp | `102` | يعرض صفحة من المستند ويحفظها كملف BMP. |
| Emf | `103` | يعرض صفحة من المستند ويحفظها كملف متجه EMF (ملف تعريف محسّن). |
| Jpeg | `104` | يعرض صفحة من المستند ويحفظها كملف JPEG. |
| Gif | `105` | يعرض صفحة من المستند ويحفظها كملف GIF. |
| Eps | `106` | يعرض صفحة من المستند ويحفظها كملف EPS. |

## أمثلة

يوضح كيفية التحويل من تنسيق DOCX إلى تنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### أنظر أيضا

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
