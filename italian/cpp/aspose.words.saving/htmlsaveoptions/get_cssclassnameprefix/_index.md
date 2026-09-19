---
title: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix"
linktitle: "get_CssClassNamePrefix"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix. Specifica un prefisso che viene aggiunto a tutti i nomi delle classi CSS. Il valore predefinito è una stringa vuota e i nomi delle classi CSS generate non hanno un prefisso comune in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_cssclassnameprefix/
---
## HtmlSaveOptions::get_CssClassNamePrefix method


Specifica un prefisso che viene aggiunto a tutti i nomi delle classi CSS. Il valore predefinito è una stringa vuota e i nomi delle classi CSS generate non hanno alcun prefisso comune.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix() const
```

## Note


Se questo valore non è vuoto, tutte le classi CSS generate da Aspose.Words inizieranno con il prefisso specificato. Questo può essere utile, ad esempio, se aggiungi CSS personalizzato ai documenti generati e desideri evitare conflitti di nomi di classi.

Se il valore non è **null** o vuoto, deve essere un identificatore CSS valido.

## Esempi



Mostra come salvare un documento in HTML e aggiungere un prefisso a tutti i suoi nomi di classi CSS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
saveOptions->set_CssClassNamePrefix(u"myprefix-");

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html");

ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Header\">"));
ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Footer\">"));

outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.css");

ASSERT_TRUE(outDocContents.Contains(u".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
ASSERT_TRUE(outDocContents.Contains(u".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
