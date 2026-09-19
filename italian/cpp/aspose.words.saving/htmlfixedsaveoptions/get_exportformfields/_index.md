---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields metodo"
linktitle: "get_ExportFormFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields metodo. Ottiene o imposta l'indicazione se i campi modulo sono esportati come elementi interattivi (come tag ''input'') anziché convertiti in testo o grafica in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


Ottiene o imposta l'indicazione se i campi modulo sono esportati come elementi interattivi (come tag 'input') anziché convertiti in testo o grafica.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## Esempi



Mostra come esportare i campi modulo in Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// Quando esportiamo un documento con campi modulo in .html,
// ci sono due modi in cui Aspose.Words può esportare i campi modulo.
// Impostare il flag "ExportFormFields" su "true" li esporterà come oggetti interattivi.
// Impostare questo flag su "false" visualizzerà i campi modulo come testo semplice.
// Ciò li bloccherà al valore corrente e impedirà al lettore del nostro documento HTML
// di poter interagire con essi.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportFormFields(exportFormFields);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")->get_Success());
}
```

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
