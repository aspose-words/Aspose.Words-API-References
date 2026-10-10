---
title: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator Methode"
linktitle: "get_CrossReferenceSeparator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator Methode. Liest oder setzt die Zeichenfolge, die verwendet wird, um Querverweise und andere Einträge in C++ zu trennen."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldindex/get_crossreferenceseparator/
---
## FieldIndex::get_CrossReferenceSeparator method


Liest oder setzt die Zeichenfolge, die verwendet wird, um Querverweise und andere Einträge zu trennen.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator()
```


## Beispiele



Zeigt, wie man Querverweise in einem INDEX-Feld definiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Text‑Eigenschaftswert des XE-Feldes auf der linken Seite an,
// und die Seitenzahl, die das XE-Feld enthält, auf der rechten Seite.
// Der INDEX-Eintrag sammelt alle XE-Felder mit übereinstimmenden Werten in der \"Text\"-Eigenschaft.
// zu einem Eintrag, anstatt für jedes XE-Feld einen eigenen Eintrag zu erstellen.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Wir können ein XE-Feld so konfigurieren, dass sein INDEX-Eintrag einen String anstelle einer Seitenzahl anzeigt.
// Zuerst für Einträge, die eine Seitenzahl durch einen String ersetzen,
// geben Sie einen benutzerdefinierten Trenner zwischen dem Text‑Eigenschaftswert des XE-Felds und dem String an.
index->set_CrossReferenceSeparator(u", see: ");

ASSERT_EQ(u" INDEX  \\k \", see: \"", index->GetFieldCode());

// Fügen Sie ein XE-Feld ein, das einen regulären INDEX-Eintrag erzeugt, der die Seitenzahl dieses Feldes anzeigt,
// und den Wert von CrossReferenceSeparator nicht verwendet.
// Der Eintrag für dieses XE-Feld wird "Apple, 2" anzeigen.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");

ASSERT_EQ(u" XE  Apple", indexEntry->GetFieldCode());

// Fügen Sie ein weiteres XE-Feld auf Seite 3 ein und setzen Sie einen Wert für die Eigenschaft PageNumberReplacement.
// Dieser Wert wird anstelle der Seitenzahl, auf der sich dieses Feld befindet, angezeigt,
// und der Wert von CrossReferenceSeparator des INDEX-Feldes erscheint davor.
// Der Eintrag für dieses XE-Feld wird "Banana, siehe: Tropische Frucht" anzeigen.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");
indexEntry->set_PageNumberReplacement(u"Tropical fruit");

ASSERT_EQ(u" XE  Banana \\t \"Tropical fruit\"", indexEntry->GetFieldCode());

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.CrossReferenceSeparator.docx");
```

## Siehe auch

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
