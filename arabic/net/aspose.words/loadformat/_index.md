---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.LoadFormat، التي تحدد تنسيقات المستندات للتحميل السلس والتوافق المعزز في تطبيقاتك.
type: docs
weight: 4000
url: /ar/net/aspose.words/loadformat/
---
## LoadFormat enumeration

يشير إلى تنسيق المستند الذي سيتم تحميله.

```csharp
public enum LoadFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Auto | `0` | يوجه Aspose.Words للتعرف على التنسيق تلقائيًا. |
| MsWorks | `8` | مستند Microsoft Works 8. |
| Doc | `10` | Microsoft Word 95 أو Word 97 - مستند 2003. |
| Dot | `11` | قالب Microsoft Word 95 أو Word 97 - 2003. |
| DocPreWord60 | `12` | المستند بتنسيق ما قبل Word 95. لا يدعم Aspose.Words حاليًا تحميل مثل هذه المستندات. |
| Docx | `20` | مستند معالجة الكلمات Office Open XML ML (خالي من وحدات الماكرو). |
| Docm | `21` | مستند Office Open XML WordprocessingML ممكّن بالماكرو. |
| Dotx | `22` | قالب معالجة الكلمات Office Open XML WordprocessingML (خالي من وحدات الماكرو). |
| Dotm | `23` | قالب Office Open XML WordprocessingML الممكّن بالماكرو. |
| FlatOpc | `24` | يتم تخزين Office Open XML WordprocessingML في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML مستند ممكّن بالماكرو يتم تخزينه في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplate | `26` | قالب Office Open XML WordprocessingML (خالي من وحدات الماكرو) مخزّن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | قالب Office Open XML WordprocessingML الممكّن بالماكرو مخزّن في ملف XML مسطح بدلاً من حزمة ZIP. |
| Rtf | `30` | تنسيق RTF. |
| WordML | `31` | معالجة الكلمات في Microsoft Word 2003 بتنسيق ML. |
| Html | `50` | تنسيق HTML. |
| Mhtml | `51` | تنسيق MHTML (أرشيف الويب). |
| Mobi | `52` | تنسيق MOBI. يُستخدم في قارئ MobiPocket وقارئات Amazon Kindle. |
| Chm | `53` | تنسيق CHM (تعليمات HTML المجمعة). |
| Azw3 | `54` | تنسيق AZW3. يستخدمه قارئو أمازون كيندل. |
| Epub | `55` | تنسيق EPUB. |
| Odt | `60` | مستند نصي ODF. |
| Ott | `61` | قالب مستند نصي ODF. |
| Text | `62` | نص عادي. |
| Markdown | `63` | مستند نصي Markdown. |
| Pdf | `64` | وثيقة PDF. |
| Xml | `65` | مستند XML . |
| Unknown | `255` | تنسيق غير معروف، لا يمكن تحميله بواسطة Aspose.Words. |

## أمثلة

يوضح كيفية حفظ صفحة الويب كملف .docx.

```csharp
const string url = "https://products.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // يتم استخدام عنوان URL مرة أخرى باعتباره Uri أساسيًا للتأكد من استرداد أي مسارات صور نسبية بشكل صحيح.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // قم بتحميل مستند HTML من الدفق ومرر كائن LoadOptions.
        Document doc = new Document(stream, options);

        // في هذه المرحلة، يمكننا قراءة محتويات المستند وتحريرها ثم حفظها في نظام الملفات المحلي.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

يوضح كيفية تحديد عنوان URI الأساسي عند فتح مستند html.

```csharp
// افترض أننا نريد تحميل مستند .html يحتوي على صورة مرتبطة بمعرف URI نسبي
// بينما الصورة في موقع مختلف. في هذه الحالة، سنحتاج إلى تحويل عنوان URI النسبي إلى عنوان URI مطلق.
 // يمكننا توفير عنوان URI أساسي باستخدام كائن HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// بينما كانت الصورة معطلة في ملف .html المدخل، ساعدنا عنوان URI الأساسي المخصص في إصلاح الرابط.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// ستعرض وثيقة الإخراج هذه الصورة المفقودة.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

يوضح كيفية استخدام طرق FileFormatUtil للكشف عن تنسيق المستند.

```csharp
// قم بتحميل مستند من ملف يفتقد ملحق الملف، ثم اكتشف تنسيق الملف الخاص به.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // فيما يلي طريقتان لتحويل LoadFormat إلى SaveFormat المقابل له.
    // 1 - احصل على سلسلة امتداد الملف لـ LoadFormat، ثم احصل على SaveFormat المقابل من تلك السلسلة:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - تحويل LoadFormat مباشرة إلى SaveFormat الخاص به:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // قم بتحميل مستند من الدفق، ثم احفظه في امتداد الملف الذي تم اكتشافه تلقائيًا.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
