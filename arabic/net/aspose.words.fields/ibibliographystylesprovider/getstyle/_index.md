---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة IBibliographyStylesProvider GetStyle لاسترجاع أنماط المراجع الخاصة بك وتخصيصها بسهولة لتحسين الكتابة الأكاديمية.
type: docs
weight: 10
url: /ar/net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

يعيد نمط الببليوغرافيا.

```csharp
public Stream GetStyle(string styleFileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| styleFileName | String | اسم ملف نمط المراجع. |

### قيمة الإرجاع

الStream مع نمط XSLT ببليوغرافيا.

## ملاحظات

يجب أن يعود التنفيذ`باطل` للإشارة إلى أنه يجب استخدام إصدار MS Word للنمط المحدد.

## أمثلة

يوضح كيفية تجاوز الأنماط المضمنة أو توفير نمط مخصص.

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // إذا كان المستند يحتوي بالفعل على نمط، فيمكنك تغييره باستخدام الكود التالي:
    // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

    doc.FieldOptions.BibliographyStylesProvider = new BibliographyStylesProvider();
    doc.UpdateFields();

    doc.Save(ArtifactsDir + "Field.ChangeBibliographyStyles.docx");

}

public class BibliographyStylesProvider : IBibliographyStylesProvider
{
    Stream IBibliographyStylesProvider.GetStyle(string styleFileName)
    {
        return File.OpenRead(MyDir + "Bibliography custom style.xsl");
    }
}
```

### أنظر أيضا

* interface [IBibliographyStylesProvider](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
