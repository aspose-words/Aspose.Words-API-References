---
title: "Aspose::Words::DocumentBuilder::InsertCheckBox Methode"
linktitle: "InsertCheckBox"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertCheckBox Methode. Fügt ein Kontrollkästchen-Formularfeld an der aktuellen Position in C++ ein."
type: docs
weight: 31000
url: /de/cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


Fügt ein Kontrollkästchen-Formularfeld an der aktuellen Position ein.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name des Formularfelds. Kann eine leere Zeichenfolge sein. Der Wert, der länger als 20 Zeichen ist, wird abgeschnitten. |
| checkedValue | bool | Geprüfter Status des Kontrollkästchen-Formularfelds. |
| size | int32_t | Gibt die Größe des Kontrollkästchens in Punkten an. Geben Sie 0 für MS Word an, damit die Größe des Kontrollkästchens automatisch berechnet wird. |

### ReturnValue

Der gerade eingefügte Formularfeldknoten.
## Hinweise


Wenn Sie einen Namen für das Formularfeld angeben, wird automatisch ein Lesezeichen mit demselben Namen erstellt.

## Beispiele



Zeigt, wie man Kontrollkästchen in das Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt Kontrollkästchen mit unterschiedlichen Größen und standardmäßig geprüften Zuständen ein.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Formularfelder haben eine Namenslängenbegrenzung von 20 Zeichen.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Wir können mit diesen Kontrollkästchen in Microsoft Word durch Doppelklicken interagieren.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Siehe auch

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


Fügt ein Kontrollkästchen-Formularfeld an der aktuellen Position ein.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name des Formularfelds. Kann eine leere Zeichenfolge sein. Der Wert, der länger als 20 Zeichen ist, wird abgeschnitten. |
| defaultValue | bool | Standardwert des Kontrollkästchen-Formularfelds. |
| checkedValue | bool | Aktueller geprüfter Status des Kontrollkästchen-Formularfelds. |
| size | int32_t | Gibt die Größe des Kontrollkästchens in Punkten an. Geben Sie 0 für MS Word an, damit die Größe des Kontrollkästchens automatisch berechnet wird. |

### ReturnValue

Der gerade eingefügte Formularfeldknoten.
## Hinweise


Wenn Sie einen Namen für das Formularfeld angeben, wird automatisch ein Lesezeichen mit demselben Namen erstellt.

## Beispiele



Zeigt, wie man Kontrollkästchen in das Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt Kontrollkästchen mit unterschiedlichen Größen und standardmäßig geprüften Zuständen ein.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Formularfelder haben eine Namenslängenbegrenzung von 20 Zeichen.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Wir können mit diesen Kontrollkästchen in Microsoft Word durch Doppelklicken interagieren.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Siehe auch

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
