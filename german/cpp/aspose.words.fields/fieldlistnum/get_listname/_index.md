---
title: "Aspose::Words::Fields::FieldListNum::get_ListName Methode"
linktitle: "get_ListName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldListNum::get_ListName-Methode. Gibt den Namen der abstrakten Nummerierungsdefinition zurück oder legt ihn fest, die für die Nummerierung in C++ verwendet wird."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fields/fieldlistnum/get_listname/
---
## FieldListNum::get_ListName method


Liest oder setzt den Namen der für die Nummerierung verwendeten abstrakten Nummerierungsdefinition.

```cpp
System::String Aspose::Words::Fields::FieldListNum::get_ListName()
```


## Beispiele



Zeigt, wie Absätze mit LISTNUM-Feldern nummeriert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// LISTNUM-Felder zeigen eine Zahl an, die bei jedem LISTNUM-Feld erhöht wird.
// Diese Felder verfügen außerdem über verschiedene Optionen, die es uns ermöglichen, sie zur Nachbildung nummerierter Listen zu verwenden.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Listen beginnen standardmäßig bei 1 zu zählen, aber wir können diese Zahl auf einen anderen Wert setzen, z. B. 0.
// Dieses Feld zeigt "0)" an.
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// LISTNUM-Felder führen separate Zähler für jede Listenebene.
// Einfügen eines LISTNUM-Feldes im selben Absatz wie ein anderes LISTNUM-Feld
// erhöht die Listenebene statt des Zählers.
// Das nächste Feld wird die Zählung, die wir oben begonnen haben, fortsetzen und einen Wert von "1" auf Listenebene 1 anzeigen.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Dieses Feld startet eine Zählung auf Listenebene 2. Es zeigt einen Wert von "1" an.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Dieses Feld startet eine Zählung auf Listenebene 3. Es zeigt einen Wert von "1" an.
// Verschiedene Listenebenen haben unterschiedliche Formatierungen,
// so werden diese Felder kombiniert einen Wert von "1)a)i)" anzeigen.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// Das nächste LISTNUM-Feld, das wir einfügen, wird die Zählung auf der Listenebene fortsetzen
// dass das vorherige LISTNUM-Feld aktiv war.
// Wir können die Eigenschaft "ListLevel" verwenden, um zu einer anderen Listenebene zu springen.
// Wenn dieses LISTNUM-Feld auf Listenebene 3 bleiben würde, würde es "ii)" anzeigen,
// aber, da wir es auf Listenebene 2 verschoben haben, führt es die Zählung auf dieser Ebene fort und zeigt "b)" an.
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Wir können die Eigenschaft ListName setzen, um das Feld einen anderen AUTONUM-Feldtyp nachahmen zu lassen.
// "NumberDefault" emuliert AUTONUM, "OutlineDefault" emuliert AUTONUMOUT,
// und "LegalDefault" emuliert AUTONUMLGL-Felder.
// Der Listename "OutlineDefault" mit 1 als Startzahl führt dazu, dass "I." angezeigt wird.
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// Der ListName wird nicht vom vorherigen Feld übernommen, daher müssen wir ihn für jedes neue Feld setzen.
// Dieses Feld setzt die Zählung mit dem anderen Listennamen fort und zeigt "II." an.
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## Siehe auch

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
