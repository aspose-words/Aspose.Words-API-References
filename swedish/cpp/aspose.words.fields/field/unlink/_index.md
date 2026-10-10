---
title: "Aspose::Words::Fields::Field::Unlink method"
linktitle: "Koppla bort"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::Field::Unlink method. Utför fältets avkoppling i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words.fields/field/unlink/
---
## Field::Unlink method


Utför avlänkning av fältet.

```cpp
bool Aspose::Words::Fields::Field::Unlink()
```


### ReturnValue

**true** if the field has been unlinked, otherwise **false**.
## Anmärkningar


Ersätter fältet med dess senaste resultat.

Vissa fält, såsom XE (Indexpost) fält och SEQ (Sekvens) fält, kan inte kopplas bort.

## Exempel



Visar hur man kopplar bort ett fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");
doc->get_Range()->get_Fields()->idx_get(1)->Unlink();
```

## Se även

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
