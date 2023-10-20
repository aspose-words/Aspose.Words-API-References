---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words لـ .NET
description: Aspose.Words.LoadFormat تعداد. يشير إلى تنسيق المستند الذي سيتم تحميله في C#.
type: docs
weight: 3550
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
| Doc | `10` | مستند Microsoft Word 95 أو Word 97 - 2003. |
| Dot | `11` | قالب Microsoft Word 95 أو Word 97 - 2003. |
| DocPreWord60 | `12` | المستند بتنسيق ما قبل Word 95. Aspose.Words لا يدعم حاليًا تحميل مثل هذه المستندات. |
| Docx | `20` | مستند Office Open XML WordprocessingML (خالي من وحدات الماكرو). |
| Docm | `21` | مستند Office Open XML WordprocessingML الممكّن بماكرو. |
| Dotx | `22` | قالب Office Open XML لمعالجة النصوص ML (خالي من وحدات الماكرو). |
| Dotm | `23` | قالب Office Open XML WordprocessingML الممكّن بماكرو. |
| FlatOpc | `24` | Office Open XML WordprocessingML المخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML مستند ممكن بماكرو ومخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplate | `26` | قالب Office Open XML WordprocessingML (خالي من وحدات الماكرو) مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | قالب Office Open XML WordprocessingML الممكّن بماكرو مخزّن في ملف XML مسطح بدلاً من حزمة ZIP. |
| Rtf | `30` | تنسيق RTF. |
| WordML | `31` | تنسيق Microsoft Word 2003 WordprocessingML. |
| Html | `50` | تنسيق HTML. |
| Mhtml | `51` | تنسيق MHTML (أرشيف الويب). |
| Mobi | `52` | تنسيق MOBI. يستخدم بواسطة قارئ MobiPocket وقارئ Amazon Kindle. |
| Chm | `53` | تنسيق CHM (تعليمات HTML المجمعة). |
| Azw3 | `54` | تنسيق AZW3. يستخدم من قبل قراء Amazon Kindle. |
| Epub | `55` | تنسيق EPUB. |
| Odt | `60` | مستند نصي بتنسيق ODF. |
| Ott | `61` | قالب مستند نصي ODF. |
| Text | `62` | نص عادي. |
| Markdown | `63` | مستند نصي تخفيض السعر. |
| Pdf | `64` | مستند PDF. |
| Xml | `65` | مستند XML. |
| Unknown | `255` | تنسيق غير معروف، لا يمكن تحميله بواسطة Aspose.Words. |

## أمثلة

يوضح كيفية حفظ صفحة ويب كملف .docx.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // يتم استخدام عنوان URL مرة أخرى باعتباره BaseUri لضمان استرداد أي مسارات صور نسبية بشكل صحيح.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // قم بتحميل مستند HTML من الدفق وتمرير كائن LoadOptions.
        Document doc = new Document(stream, options);

        // في هذه المرحلة، يمكننا قراءة محتويات المستند وتحريرها ثم حفظها في نظام الملفات المحلي.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

يوضح كيفية تحديد عنوان URI أساسي عند فتح مستند html.

```csharp
// لنفترض أننا نريد تحميل مستند .html يحتوي على صورة مرتبطة بمعرف URI نسبي
// أثناء وجود الصورة في موقع مختلف. في هذه الحالة، سنحتاج إلى تحويل معرف URI النسبي إلى عنوان مطلق.
 // يمكننا توفير عنوان URI أساسي باستخدام كائن HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// أثناء تعطل الصورة في ملف الإدخال .html، ساعدنا عنوان URI الأساسي المخصص لدينا في إصلاح الرابط.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// سيعرض مستند الإخراج هذا الصورة المفقودة.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

يوضح كيفية استخدام أساليب FileFormatUtil للكشف عن تنسيق المستند.

```csharp
// قم بتحميل مستند من ملف يفتقد امتداد الملف، ثم اكتشف تنسيق الملف الخاص به.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // فيما يلي طريقتان لتحويل LoadFormat إلى SaveFormat المطابق له.
    // 1 - احصل على سلسلة امتداد الملف لـ LoadFormat، ثم احصل على SaveFormat المقابل من تلك السلسلة:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - تحويل LoadFormat مباشرةً إلى SaveFormat الخاص به:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // قم بتحميل مستند من الدفق، ثم احفظه في ملحق الملف الذي تم اكتشافه تلقائيًا.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
