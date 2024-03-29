---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words لـ .NET
description: FieldOptions BibliographyStylesProvider ملكية. الحصول على أو تعيين موفر يُرجع نمط المراجع لـ FieldBibliography وFieldCitation الحقول في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

الحصول على أو تعيين موفر يُرجع نمط المراجع لـ [`FieldBibliography`](../../fieldbibliography/) و[`FieldCitation`](../../fieldcitation/) الحقول.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

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

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
