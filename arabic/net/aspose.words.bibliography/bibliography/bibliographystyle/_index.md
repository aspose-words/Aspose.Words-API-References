---
title: Bibliography.BibliographyStyle
linktitle: BibliographyStyle
articleTitle: BibliographyStyle
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BibliographyStyle لإدارة وتخصيص النمط النشط لمراجعك بسهولة لتحسين التنظيم والعرض.
type: docs
weight: 10
url: /ar/net/aspose.words.bibliography/bibliography/bibliographystyle/
---
## Bibliography.BibliographyStyle property

يحصل على سلسلة تمثل اسم النمط النشط الذي سيتم استخدامه للمراجع أو يعينها.

```csharp
public string BibliographyStyle { get; set; }
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

* class [Bibliography](../)
* مساحة الاسم [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* المجسم [Aspose.Words](../../../)
