---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.IBibliographyStylesProvider واجهه المستخدم. قم بتنفيذ هذه الواجهة لتوفير نمط المراجع لـ FieldBibliography وFieldCitation الحقول عند تحديثها في C#.
type: docs
weight: 2670
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
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | إرجاع نمط المراجع. |

## أمثلة

يوضح كيفية تجاوز الأنماط المضمنة أو توفير أنماط مخصصة.

```csharp
public void ChangeBibliographyStyles()
{            
    Document doc = new Document(MyDir + "Bibliography.docx");

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
