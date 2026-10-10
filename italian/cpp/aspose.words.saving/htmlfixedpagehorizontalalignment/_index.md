---
title: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum"
linktitle: "HtmlFixedPageHorizontalAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum. Specifica l'allineamento orizzontale per le pagine nel documento HTML di output in C++."
type: docs
weight: 59000
url: /it/cpp/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enum


Specifica l'allineamento orizzontale delle pagine nel documento HTML di output.

```cpp
enum class HtmlFixedPageHorizontalAlignment
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Sinistra | 0 | Allinea le pagine a sinistra. |
| Centro | 1 | Centra le pagine. Questo è il valore predefinito. |
| Destra | 2 | Allinea le pagine a destra. |


## Esempi



Mostra come impostare l'allineamento orizzontale delle pagine durante il salvataggio di un documento in HTML.
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

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
