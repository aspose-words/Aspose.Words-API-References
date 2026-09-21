---
title: "Aspose::Words::Paragraph::AppendField method"
linktitle: "AppendField"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Paragraph::AppendField method. Lägger till ett fält i detta stycke i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


Lägger till ett fält i detta stycke.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Typen av fältet som ska läggas till. |
| updateField | bool | Anger om fältet ska uppdateras omedelbart. |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det tillagda fältet.

## Exempel



Visar olika sätt att lägga till fält i ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Nedan följer tre sätt att lägga till ett fält i slutet av ett stycke.
// 1 -  Lägg till ett DATE‑fält med en fälttyp och uppdatera det sedan:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Lägg till ett TIME‑fält med en fältkod:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Lägg till ett QUOTE‑fält med en fältkod, och få det att visa ett platshållarvärde:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


Lägger till ett fält i detta stycke.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | const System::String\& | Fältkoden att lägga till (utan måsvingar). |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det tillagda fältet.

## Exempel



Visar olika sätt att lägga till fält i ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Nedan följer tre sätt att lägga till ett fält i slutet av ett stycke.
// 1 -  Lägg till ett DATE‑fält med en fälttyp och uppdatera det sedan:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Lägg till ett TIME‑fält med en fältkod:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Lägg till ett QUOTE‑fält med en fältkod, och få det att visa ett platshållarvärde:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


Lägger till ett fält i detta stycke.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | const System::String\& | Fältkoden att lägga till (utan måsvingar). |
| fieldValue | const System::String\& | Fältvärdet att lägga till. Skicka **null** för fält som inte har något värde. |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det tillagda fältet.

## Exempel



Visar olika sätt att lägga till fält i ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Nedan följer tre sätt att lägga till ett fält i slutet av ett stycke.
// 1 -  Lägg till ett DATE‑fält med en fälttyp och uppdatera det sedan:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Lägg till ett TIME‑fält med en fältkod:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Lägg till ett QUOTE‑fält med en fältkod, och få det att visa ett platshållarvärde:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
