---
title: "Aspose::Words::Fields::TextFormFieldType enum"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::TextFormFieldType enum. Gibt den Typ eines Textformularfelds in C++ an."
type: docs
weight: 134000
url: /de/cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


Gibt den Typ eines Textformularfelds an.

```cpp
enum class TextFormFieldType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Regular | 0 | Das Textformularfeld kann beliebigen Text enthalten. |
| Number | 1 | Das Textformularfeld kann nur Zahlen enthalten. |
| Datum | 2 | Das Textformularfeld kann nur einen gültigen Datumswert enthalten. |
| CurrentDate | 3 | Der Wert des Textformularfelds ist das aktuelle Datum, wenn das Feld aktualisiert wird. |
| CurrentTime | 4 | Der Wert des Textformularfelds ist die aktuelle Uhrzeit, wenn das Feld aktualisiert wird. |
| Calculated | 5 | Der Wert des Textformularfelds wird aus dem Ausdruck berechnet, der in der Eigenschaft [TextInputDefault](../formfield/get_textinputdefault/) angegeben ist. |


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

## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
