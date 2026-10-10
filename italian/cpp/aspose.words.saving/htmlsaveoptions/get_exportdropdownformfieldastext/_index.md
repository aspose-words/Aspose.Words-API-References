---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText metodo"
linktitle: "get_ExportDropDownFormFieldAsText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText. Controlla come i campi modulo a discesa vengono salvati in HTML o MHTML. Il valore predefinito è false in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


Controlla come i campi modulo a discesa vengono salvati in HTML o MHTML. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## Note


Quando impostato su **true**, esporta i campi modulo a discesa come testo normale. Quando **false**, esporta i campi modulo a discesa come elemento SELECT in HTML.

Durante l'esportazione in EPUB, i campi modulo a discesa di tipo testo vengono sempre salvati come testo a causa dei requisiti di questo formato.

## Esempi



Mostra come far sì che i campi modulo a discesa del combo box si integrino con il testo del paragrafo durante il salvataggio in html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilizza un document builder per inserire un combo box con il valore "Two" selezionato.
builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"One", u"Two", u"Three"}), 1);

// Il flag "ExportDropDownFormFieldAsText" di questo oggetto SaveOptions ci consente di
// controllare come il salvataggio del documento in HTML gestisce i combo box a discesa.
// Impostandolo su "true" convertirà ogni combo box in testo semplice
// che mostra il valore attualmente selezionato del combo box, congelandolo efficacemente.
// Impostandolo su "false" manterrà la funzionalità del combo box utilizzando i tag <select> e <option>.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Two</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<select name=\"MyComboBox\">") + u"<option>One</option>" + u"<option selected=\"selected\">Two</option>" + u"<option>Three</option>" + u"</select>"));
}
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
