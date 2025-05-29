---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.WarningSource enum، الذي يحدد مصادر التحذير أثناء تحميل المستندات وحفظها لتحسين إدارة المستندات.
type: docs
weight: 7500
url: /ar/net/aspose.words/warningsource/
---
## WarningSource enumeration

يحدد الوحدة التي تنتج تحذيرًا أثناء تحميل المستند أو حفظه.

```csharp
public enum WarningSource
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Unknown | `0` | لم يتم تحديد مصدر التحذير. |
| Layout | `1` | وحدة تقوم ببناء تخطيط مستند. |
| DrawingML | `2` | وحدة تقوم بعرض أشكال DrawingML. |
| OfficeMath | `3` | وحدة تقوم بعرض OfficeMath. |
| Shapes | `4` | وحدة تقوم بمعالجة الأشكال العادية. |
| Metafile | `5` | وحدة تقوم بعرض الملفات التعريفية. |
| Xps | `6` | وحدة تقوم بعرض XPS. |
| Pdf | `7` | وحدة تقوم بعرض ملفات PDF. |
| Image | `8` | وحدة لعرض الصور. |
| Docx | `9` | وحدة تقرأ/تكتب ملفات DOCX. |
| Doc | `10` | وحدة تقوم بقراءة/كتابة ملفات DOC الثنائية. |
| Text | `11` | وحدة تقوم بقراءة/كتابة ملفات النص العادي. |
| Rtf | `12` | وحدة تقرأ/تكتب ملفات RTF. |
| WordML | `13` | وحدة تقرأ/تكتب ملفات WML. |
| Nrx | `14` | وحدات مشتركة بين وحدات قراءة/كتابة DOCX/WML. |
| Odt | `15` | وحدة تقوم بقراءة/كتابة ملفات ODT. |
| Html | `16` | وحدة تقرأ/تكتب ملفات HTML/MHTML. |
| Validator | `17` | وحدة للتحقق من اتساق النموذج وصلاحيته. |
| Xaml | `18` | وحدة تقوم بقراءة/كتابة ملفات Xaml. |
| Svm | `19` | وحدة تقرأ ملفات Svm. |
| MathML | `20` | وحدة تقرأ ملفات W3C MathML. |
| Font | `21` | وحدة تقرأ ملفات الخطوط. |
| Svg | `22` | وحدة تقرأ ملفات SVG. |
| Markdown | `23` | وحدة تقوم بقراءة/كتابة ملفات Markdown. |
| Chm | `24` | وحدة تقرأ ملفات CHM. |
| Epub | `25` | وحدة تقرأ/تكتب ملفات EPUB. |
| Xml | `26` | وحدة تقرأ ملفات XML. |
| Xlsx | `27` | وحدة تكتب ملفات XLSX. |

## أمثلة

يوضح كيفية العمل مع مصدر التحذير.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
