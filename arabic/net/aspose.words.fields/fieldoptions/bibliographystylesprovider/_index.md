---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldOptions BibliographyStylesProvider للحصول على أنماط ببليوغرافية قابلة للتخصيص، مما يعزز حقول FieldBibliography وFieldCitation.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

يحصل على أو يعين موفرًا يعيد نمط ببليوغرافيا لـ [`FieldBibliography`](../../fieldbibliography/) و[`FieldCitation`](../../fieldcitation/) الحقول.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

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

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
