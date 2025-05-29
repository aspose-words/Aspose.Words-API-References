---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words لـ .NET
description: قم بتعزيز تنسيق مستندك باستخدام واجهة Aspose.Words.IBibliographyStylesProvider، وهي مثالية لتخصيص أنماط المراجع في الاستشهادات.
type: docs
weight: 3080
url: /ar/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

قم بتنفيذ هذه الواجهة لتوفير نمط المراجع لـ [`FieldBibliography`](../fieldbibliography/) و[`FieldCitation`](../fieldcitation/) الحقول عند تحديثها.

```csharp
public interface IBibliographyStylesProvider
```

## طُرق

| اسم | وصف |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | يعيد نمط الببليوغرافيا. |

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

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
