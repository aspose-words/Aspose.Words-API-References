---
title: "Aspose::Words::Paragraph::InsertField Methode"
linktitle: "InsertField"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::InsertField Methode. Fügt ein Feld in diesen Absatz in C++ ein."
type: docs
weight: 29000
url: /de/cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Fügt ein Feld in diesen Absatz ein.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Der Typ des einzufügenden Feldes. |
| updateField | bool | Gibt an, ob das Feld sofort aktualisiert werden soll. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Referenzknoten innerhalb dieses Absatzes (wenn *refNode* **null** ist, wird er am Ende des Absatzes angehängt). |
| isAfter | bool | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/)-Objekt, das das eingefügte Feld darstellt.

## Beispiele



Zeigt verschiedene Möglichkeiten, Felder zu einem Absatz hinzuzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Unten sind drei Möglichkeiten, ein Feld in einen Absatz einzufügen.
// 1 -  Fügen Sie ein AUTHOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Fügen Sie ein QUOTE-Feld nach einem der untergeordneten Knoten des Absatzes ein:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Fügen Sie ein QUOTE-Feld vor einem der untergeordneten Knoten des Absatzes ein,
// und lassen Sie es einen Platzhalterwert anzeigen:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Fügt ein Feld in diesen Absatz ein.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | const System::String\& | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Referenzknoten innerhalb dieses Absatzes (wenn *refNode* **null** ist, wird er am Ende des Absatzes angehängt). |
| isAfter | bool | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/)-Objekt, das das eingefügte Feld darstellt.

## Beispiele



Zeigt verschiedene Möglichkeiten, Felder zu einem Absatz hinzuzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Unten sind drei Möglichkeiten, ein Feld in einen Absatz einzufügen.
// 1 -  Fügen Sie ein AUTHOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Fügen Sie ein QUOTE-Feld nach einem der untergeordneten Knoten des Absatzes ein:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Fügen Sie ein QUOTE-Feld vor einem der untergeordneten Knoten des Absatzes ein,
// und lassen Sie es einen Platzhalterwert anzeigen:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Fügt ein Feld in diesen Absatz ein.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | const System::String\& | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| fieldValue | const System::String\& | Der Feldwert, der eingefügt werden soll. Übergeben Sie **null** für Felder, die keinen Wert haben. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Referenzknoten innerhalb dieses Absatzes (wenn *refNode* **null** ist, wird er am Ende des Absatzes angehängt). |
| isAfter | bool | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/)-Objekt, das das eingefügte Feld darstellt.

## Beispiele



Zeigt verschiedene Möglichkeiten, Felder zu einem Absatz hinzuzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Unten sind drei Möglichkeiten, ein Feld in einen Absatz einzufügen.
// 1 -  Fügen Sie ein AUTHOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Fügen Sie ein QUOTE-Feld nach einem der untergeordneten Knoten des Absatzes ein:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Fügen Sie ein QUOTE-Feld vor einem der untergeordneten Knoten des Absatzes ein,
// und lassen Sie es einen Platzhalterwert anzeigen:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
