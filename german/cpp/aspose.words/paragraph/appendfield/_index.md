---
title: "Aspose::Words::Paragraph::AppendField Methode"
linktitle: "AppendField"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::AppendField Methode. Fügt diesem Absatz ein Feld hinzu in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


Fügt diesem Absatz ein Feld hinzu.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Der Typ des anzuhängenden Feldes. |
| updateField | bool | Gibt an, ob das Feld sofort aktualisiert werden soll. |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/) Objekt, das das angefügte Feld darstellt.

## Beispiele



Zeigt verschiedene Möglichkeiten, Felder zu einem Absatz hinzuzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Unten sind drei Methoden aufgeführt, ein Feld am Ende eines Absatzes hinzuzufügen.
// 1 -  Ein DATE-Feld mithilfe eines Feldtyps anhängen und anschließend aktualisieren:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Ein TIME-Feld mithilfe eines Feldcodes anhängen:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Ein QUOTE-Feld mithilfe eines Feldcodes anhängen und es zur Anzeige eines Platzhalterwerts bringen:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


Fügt diesem Absatz ein Feld hinzu.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | const System::String\& | Der Feldcode, der angehängt werden soll (ohne geschweifte Klammern). |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/) Objekt, das das angefügte Feld darstellt.

## Beispiele



Zeigt verschiedene Möglichkeiten, Felder zu einem Absatz hinzuzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Unten sind drei Methoden aufgeführt, ein Feld am Ende eines Absatzes hinzuzufügen.
// 1 -  Ein DATE-Feld mithilfe eines Feldtyps anhängen und anschließend aktualisieren:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Ein TIME-Feld mithilfe eines Feldcodes anhängen:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Ein QUOTE-Feld mithilfe eines Feldcodes anhängen und es zur Anzeige eines Platzhalterwerts bringen:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


Fügt diesem Absatz ein Feld hinzu.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | const System::String\& | Der Feldcode, der angehängt werden soll (ohne geschweifte Klammern). |
| fieldValue | const System::String\& | Der Feldwert, der angehängt werden soll. Übergeben Sie **null** für Felder, die keinen Wert haben. |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/) Objekt, das das angefügte Feld darstellt.

## Beispiele



Zeigt verschiedene Möglichkeiten, Felder zu einem Absatz hinzuzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Unten sind drei Methoden aufgeführt, ein Feld am Ende eines Absatzes hinzuzufügen.
// 1 -  Ein DATE-Feld mithilfe eines Feldtyps anhängen und anschließend aktualisieren:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Ein TIME-Feld mithilfe eines Feldcodes anhängen:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Ein QUOTE-Feld mithilfe eines Feldcodes anhängen und es zur Anzeige eines Platzhalterwerts bringen:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
