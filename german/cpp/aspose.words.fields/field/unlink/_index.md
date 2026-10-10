---
title: "Aspose::Words::Fields::Field::Unlink Methode"
linktitle: "Unlink"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::Field::Unlink Methode. Führt das Aufheben der Feldverknüpfung in C++ aus."
type: docs
weight: 22000
url: /de/cpp/aspose.words.fields/field/unlink/
---
## Field::Unlink method


Führt das Entlinken des Feldes aus.

```cpp
bool Aspose::Words::Fields::Field::Unlink()
```


### ReturnValue

**true** if the field has been unlinked, otherwise **false**.
## Hinweise


Ersetzt das Feld durch sein zuletzt erhaltenes Ergebnis.

Einige Felder, wie XE‑ (Indexeintrag) Felder und SEQ‑ (Sequenz) Felder, können nicht entkoppelt werden.

## Beispiele



Zeigt, wie man ein Feld entkoppelt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");
doc->get_Range()->get_Fields()->idx_get(1)->Unlink();
```

## Siehe auch

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
