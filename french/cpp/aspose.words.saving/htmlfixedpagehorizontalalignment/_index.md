---
title: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum"
linktitle: "HtmlFixedPageHorizontalAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum. Spécifie l'alignement horizontal des pages dans le document HTML de sortie en C++."
type: docs
weight: 59000
url: /fr/cpp/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enum


Spécifie l'alignement horizontal des pages dans le document HTML de sortie.

```cpp
enum class HtmlFixedPageHorizontalAlignment
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Gauche | 0 | Alignez les pages à gauche. |
| Centre | 1 | Centrer les pages. C'est la valeur par défaut. |
| Droite | 2 | Alignez les pages à droite. |


## Exemples



Montre comment définir l'alignement horizontal des pages lors de l'enregistrement d'un document au format HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_PageHorizontalAlignment(pageHorizontalAlignment);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment::Center:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment::Left:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment::Right:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }")->get_Success());
        break;

}
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
