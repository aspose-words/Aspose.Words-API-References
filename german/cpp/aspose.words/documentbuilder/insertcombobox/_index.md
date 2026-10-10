---
title: "Aspose::Words::DocumentBuilder::InsertComboBox method"
linktitle: "InsertComboBox"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertComboBox-Methode. Fügt ein Kombinationsfeld-Formularfeld an der aktuellen Position in C++ ein."
type: docs
weight: 32000
url: /de/cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


Fügt ein Kombinationsfeld-Formularfeld an der aktuellen Position ein.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name des Formularfelds. Kann eine leere Zeichenfolge sein. Der Wert, der länger als 20 Zeichen ist, wird abgeschnitten. |
| items | const System::ArrayPtr\<System::String\>\& | Die Elemente der ComboBox. Maximal 25 Elemente. |
| selectedIndex | int32_t | Der Index des ausgewählten Elements in der ComboBox. |

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


Zeigt, wie ein Kombinationsfeld-Formularfeld in ein Dokument eingefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt ein Formular ein, das den Benutzer auffordert, einen der Einträge aus dem Menü auszuwählen.
builder->Write(u"Pick a fruit: ");
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertComboBox.docx");
```

## Siehe auch

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
