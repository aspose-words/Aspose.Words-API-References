---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText Methode"
linktitle: "get_ExportDropDownFormFieldAsText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText Methode. Steuert, wie Dropdown-Formularfelder in HTML oder MHTML gespeichert werden. Der Standardwert ist false in C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


Steuert, wie Dropdown-Formularfelder nach HTML oder MHTML gespeichert werden. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## Hinweise


Wenn auf **true** gesetzt, werden Dropdown-Formularfelder als normaler Text exportiert. Wenn **false**, werden Dropdown-Formularfelder als SELECT-Element in HTML exportiert.

Beim Exportieren nach EPUB werden Text-Dropdown-Formularfelder immer als Text gespeichert, aufgrund der Anforderungen dieses Formats.

## Beispiele



Zeigt, wie man Dropdown-Combo-Box-Formularfelder beim Speichern nach HTML nahtlos in den Absatztext einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Verwenden Sie einen DocumentBuilder, um eine Combo-Box mit dem ausgewählten Wert "Two" einzufügen.
builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"One", u"Two", u"Three"}), 1);

// Das "ExportDropDownFormFieldAsText"-Flag dieses SaveOptions-Objekts ermöglicht es uns,
// zu steuern, wie das Speichern des Dokuments nach HTML Dropdown-Combo-Boxen behandelt.
// Wenn es auf "true" gesetzt wird, wird jede Combo-Box in einfachen Text umgewandelt
// der den aktuell ausgewählten Wert der Combo-Box anzeigt und ihn damit effektiv einfriert.
// Wenn es auf "false" gesetzt wird, bleibt die Funktionalität der Combo-Box erhalten, indem <select>- und <option>-Tags verwendet werden.
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

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
