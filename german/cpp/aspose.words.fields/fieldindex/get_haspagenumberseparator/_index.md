---
title: "Aspose::Words::Fields::FieldIndex::get_HasPageNumberSeparator Methode"
linktitle: "get_HasPageNumberSeparator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIndex::get_HasPageNumberSeparator Methode. Gibt einen Wert zurück, der angibt, ob ein Seitenzahltrennzeichen durch den Code des Feldes in C++ überschrieben wird."
type: docs
weight: 5000
url: /de/cpp/aspose.words.fields/fieldindex/get_haspagenumberseparator/
---
## FieldIndex::get_HasPageNumberSeparator method


Liest einen Wert, der angibt, ob ein Seitenzahltrennzeichen durch den Feldcode überschrieben wird.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_HasPageNumberSeparator()
```


## Beispiele



Zeigt, wie man den Seitenzahltrenner in einem INDEX-Feld bearbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Text‑Eigenschaftswert des XE-Feldes auf der linken Seite an,
// und die Seitenzahl, die das XE-Feld enthält, auf der rechten Seite.
// Der INDEX-Eintrag gruppiert XE-Felder mit übereinstimmenden Werten in der "Text"-Eigenschaft.
// zu einem Eintrag, anstatt für jedes XE-Feld einen eigenen Eintrag zu erstellen.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Wenn unser INDEX-Feld einen Eintrag für eine Gruppe von XE-Feldern hat,
// zeigt dieser Eintrag die Seitenzahl jeder Seite an, die ein XE-Feld enthält, das zu dieser Gruppe gehört.
// Wir können benutzerdefinierte Trenner festlegen, um das Aussehen dieser Seitenzahlen anzupassen.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageNumberListSeparator(u" & ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\l \" & \"", index->GetFieldCode());
ASSERT_TRUE(index->get_HasPageNumberSeparator());

// Nachdem wir diese XE-Felder eingefügt haben, zeigt das INDEX-Feld "Erster Eintrag, auf Seite(n) 2 & 3 & 4" an.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

ASSERT_EQ(u" XE  \"First entry\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageNumberList.docx");
```

## Siehe auch

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
