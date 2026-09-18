---
title: "Aspose::Words::Fields::FieldListNum Klasse"
linktitle: "FieldListNum"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldListNum Klasse. Implementiert das LISTNUM-Feld. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 64000
url: /de/cpp/aspose.words.fields/fieldlistnum/
---
## FieldListNum class


Implementiert das LISTNUM-Feld. Weitere Informationen finden Sie im [Arbeiten mit Feldern](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldListNum : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_HasListName](./get_haslistname/)() | Gibt einen Wert zurück, der angibt, ob der Name einer abstrakten Nummerierungsdefinition vom Feldcode bereitgestellt wird. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_ListLevel](./get_listlevel/)() | Liest oder setzt die Ebene in der Liste und überschreibt das Standardverhalten des Feldes. |
| [get_ListName](./get_listname/)() | Liest oder setzt den Namen der für die Nummerierung verwendeten abstrakten Nummerierungsdefinition. |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_StartingNumber](./get_startingnumber/)() | Liest oder setzt den Startwert für dieses Feld. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() override | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_ListLevel](./set_listlevel/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldListNum::get_ListLevel](./get_listlevel/). |
| [set_ListName](./set_listname/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldListNum::get_ListName](./get_listname/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_StartingNumber](./set_startingnumber/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldListNum::get_StartingNumber](./get_startingnumber/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
