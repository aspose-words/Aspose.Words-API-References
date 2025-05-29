---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.SaveFormat enum لاختيار تنسيقات حفظ المستندات بسهولة، مما يعزز إدارة الملفات لديك والتوافق لضمان سير العمل بسلاسة.
type: docs
weight: 5580
url: /ar/net/aspose.words/saveformat/
---
## SaveFormat enumeration

يشير إلى التنسيق الذي تم حفظ المستند به.

```csharp
public enum SaveFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Unknown | `0` | افتراضيًا، قيمة غير صالحة لتنسيق الملف. |
| Doc | `10` | يحفظ المستند بتنسيق مستند Microsoft Word 97 - 2007. |
| Dot | `11` | يحفظ المستند بتنسيق قالب Microsoft Word 97 - 2007. |
| Docx | `20` | يحفظ المستند كمستند Office Open XML WordprocessingML (خالي من وحدات الماكرو). |
| Docm | `21` | يحفظ المستند كمستند Office Open XML WordprocessingML ممكّن للماكرو. |
| Dotx | `22` | يحفظ المستند كقالب Office Open XML WordprocessingML (خالي من وحدات الماكرو). |
| Dotm | `23` | يحفظ المستند كقالب Office Open XML WordprocessingML Macro-Enabled. |
| FlatOpc | `24` | يحفظ المستند بتنسيق Office Open XML WordprocessingML مخزّنًا في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcMacroEnabled | `25` | يحفظ المستند كمستند Office Open XML WordprocessingML Macro-Enabled، ويُخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplate | `26` | يحفظ المستند كقالب Office Open XML WordprocessingML (خالي من وحدات الماكرو) مخزنًا في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | يحفظ المستند كقالب Office Open XML WordprocessingML Macro-Enabled مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| Rtf | `30` | يحفظ المستند بتنسيق RTF. يتم تحويل جميع الأحرف التي يزيد طولها عن 7 بتات إلى أحرف سداسية عشرية أو أحرف Unicode. |
| WordML | `31` | يحفظ المستند بتنسيق Microsoft Word 2003 WordprocessingML. |
| Pdf | `40` | يحفظ المستند بتنسيق PDF (Adobe Portable Document). |
| Xps | `41` | يحفظ المستند بتنسيق XPS (مواصفات ورق XML). |
| XamlFixed | `42` | يحفظ المستند بتنسيق لغة ترميز التطبيقات القابلة للتوسيع (XAML) كمستند ثابت. |
| Svg | `44` | يحفظ المستند بتنسيق Svg (رسومات متجهية قابلة للتطوير). |
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
| Text | `70` | يحفظ المستند بتنسيق نص عادي. |
| XamlFlow | `71` | **بيتا.** يحفظ المستند بتنسيق لغة ترميز التطبيقات القابلة للتوسيع (XAML) كمستند تدفق. |
| XamlFlowPack | `72` | **بيتا.** يحفظ المستند بتنسيق حزمة لغة ترميز التطبيقات القابلة للتوسيع (XAML) كمستند تدفق. |
| Markdown | `73` | يحفظ المستند بتنسيق Markdown. |
| Xlsx | `80` | يحفظ المستند كمستند Office Open XML SpreadsheetML (خالي من وحدات الماكرو). |
| Tiff | `100` | يقوم بعرض صفحة أو صفحات من المستند وحفظها في ملف TIFF أحادي أو متعدد الصفحات. |
| Png | `101` | يقوم بعرض صفحة من المستند وحفظها كملف PNG. |
| Bmp | `102` | يقوم بعرض صفحة من المستند وحفظها كملف BMP. |
| Emf | `103` | يقوم بعرض صفحة من المستند وحفظها كملف EMF (ملف ميتا معزز) متجه. |
| Jpeg | `104` | يقوم بعرض صفحة من المستند وحفظها كملف JPEG. |
| Gif | `105` | يقوم بعرض صفحة من المستند وحفظها كملف GIF. |
| Eps | `106` | يقوم بعرض صفحة من المستند وحفظها كملف EPS. |
| WebP | `107` | يقوم بعرض صفحة من المستند وحفظها كملف WebP. |

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
