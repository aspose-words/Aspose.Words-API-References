---
title: "Aspose::Words::DocumentBuilder::InsertTextInput-Methode"
linktitle: "InsertTextInput"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertTextInput-Methode. Fügt ein Textformularfeld an der aktuellen Position in C++ ein."
type: docs
weight: 49000
url: /de/cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


Fügt ein Textformularfeld an der aktuellen Position ein.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name des Formularfeldes. Kann eine leere Zeichenkette sein. |
| Typ | Aspose::Words::Fields::TextFormFieldType | Gibt den Typ des Textformularfeldes an. |
| Format | const System::String\& | Formatzeichenfolge, die zum Formatieren des Werts des Formularfeldes verwendet wird. |
| fieldValue | const System::String\& | Text, der im Feld angezeigt wird. |
| maxLength | int32_t | Maximale Länge, die der Benutzer in das Formularfeld eingeben kann. Auf Null setzen für unbegrenzte Länge. |

### ReturnValue

Der gerade eingefügte Formularfeldknoten.
## Hinweise


Wenn Sie einen Namen für das Formularfeld angeben, wird automatisch ein Lesezeichen mit demselben Namen erstellt.

## Beispiele



Zeigt, wie man Formularfelder erstellt.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Formularfelder sind Objekte im Dokument, mit denen der Benutzer interagieren kann, indem er aufgefordert wird, Werte einzugeben.
// Wir können sie mit einem Dokument-Builder erstellen, und unten sind zwei Möglichkeiten dafür aufgeführt.
// 1 -  Einfache Texteingabe:
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  Kombinationsfeld mit Hinweistext und einer Reihe möglicher Werte:
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```


Zeigt, wie man ein Text-Eingabeformularfeld in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt ein Formular ein, das den Benutzer zur Eingabe von Text auffordert.
builder->InsertTextInput(u"TextInput", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTextInput.docx");
```


Zeigt, wie man ein Text-Eingabeformularfeld einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// Fügt ein Text-Eingabefeld ein, das dem Benutzer ermöglicht, es anzuklicken und Text einzugeben.
// Weisen Sie einen Platzhaltertext zu, den der Benutzer überschreiben und übergeben kann
// eine maximale Textlänge von 0, um keine Begrenzung für den Inhalt des Formularfeldes anzuwenden.
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Das Formularfeld wird in Form eines \"input\"-HTML-Tags mit dem Typ \"text\" angezeigt.
doc->Save(get_ArtifactsDir() + u"FormFields.TextInput.html");
```

## Siehe auch

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
