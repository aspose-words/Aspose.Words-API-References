---
title: "Aspose::Words::Fields::FieldBuilder::AddArgument Methode"
linktitle: "AddArgument"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldBuilder::AddArgument Methode. Fügt das field''s Argument, das durch FieldArgumentBuilder dargestellt wird, zum field''s Code in C++ hinzu."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldbuilder/addargument/
---
## FieldBuilder::AddArgument(const System::SharedPtr\<Aspose::Words::Fields::FieldArgumentBuilder\>\&) method


Fügt das Argument eines Feldes hinzu, das durch [FieldArgumentBuilder](../../fieldargumentbuilder/) dargestellt wird, zum Code des Feldes.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(const System::SharedPtr<Aspose::Words::Fields::FieldArgumentBuilder> &argument)
```


## Beispiele



Zeigt, wie Felder mit einem Field Builder erstellt und anschließend in das Dokument eingefügt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nachfolgend finden Sie drei Beispiele für die Feldkonstruktion mit einem Field Builder.
// 1 -  Einzelnes Feld:
// Verwenden Sie einen Field Builder, um ein SYMBOL-Feld hinzuzufügen, das das ƒ (Florin)-Symbol anzeigt.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Verschachteltes Feld:
// Verwenden Sie einen Field Builder, um ein Formel-Feld zu erstellen, das von einem anderen Field Builder als inneres Feld verwendet wird.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Erstellen Sie einen weiteren Builder für ein weiteres SYMBOL-Feld und fügen Sie das Formel-Feld ein
// das wir oben erstellt haben, in das SYMBOL-Feld als Argument ein.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Das äußere SYMBOL-Feld wird das Ergebnis des Formel-Feldes, 174, als Argument verwenden,
// was dazu führt, dass das Feld das ® (Registered Sign)-Symbol anzeigt, da seine Zeichen‑Nummer 174 ist.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Mehrere verschachtelte Felder und Argumente:
// Jetzt werden wir einen Builder verwenden, um ein IF-Feld zu erstellen, das einen von zwei benutzerdefinierten Zeichenkettenwerten anzeigt,
// abhängig vom Wahr/Falsch‑Wert seines Ausdrucks. Um einen Wahr/Falsch‑Wert zu erhalten
// der bestimmt, welche Zeichenkette das IF-Feld anzeigt, wird das IF-Feld zwei numerische Ausdrücke auf Gleichheit prüfen.
// Wir werden die beiden Ausdrücke in Form von Formel‑Feldern bereitstellen, die wir innerhalb des IF-Feldes verschachteln.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Als Nächstes werden wir zwei Feldargumente erstellen, die als Wahr/Falsch‑Ausgabezeichenketten für das IF-Feld dienen.
// Diese Argumente werden die Ausgabewerte unserer numerischen Ausdrücke wiederverwenden.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Abschließend werden wir einen weiteren Field Builder für das IF-Feld erstellen und alle Ausdrücke kombinieren.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Siehe auch

* Class [FieldBuilder](../)
* Class [FieldArgumentBuilder](../../fieldargumentbuilder/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(const System::SharedPtr\<Aspose::Words::Fields::FieldBuilder\>\&) method


Fügt ein untergeordnetes Feld hinzu, das durch einen anderen [FieldBuilder](../) dargestellt wird, zum Code des Feldes.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(const System::SharedPtr<Aspose::Words::Fields::FieldBuilder> &argument)
```


## Beispiele



Zeigt, wie Felder mit einem Field Builder erstellt und anschließend in das Dokument eingefügt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nachfolgend finden Sie drei Beispiele für die Feldkonstruktion mit einem Field Builder.
// 1 -  Einzelnes Feld:
// Verwenden Sie einen Field Builder, um ein SYMBOL-Feld hinzuzufügen, das das ƒ (Florin)-Symbol anzeigt.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Verschachteltes Feld:
// Verwenden Sie einen Field Builder, um ein Formel-Feld zu erstellen, das von einem anderen Field Builder als inneres Feld verwendet wird.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Erstellen Sie einen weiteren Builder für ein weiteres SYMBOL-Feld und fügen Sie das Formel-Feld ein
// das wir oben erstellt haben, in das SYMBOL-Feld als Argument ein.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Das äußere SYMBOL-Feld wird das Ergebnis des Formel-Feldes, 174, als Argument verwenden,
// was dazu führt, dass das Feld das ® (Registered Sign)-Symbol anzeigt, da seine Zeichen‑Nummer 174 ist.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Mehrere verschachtelte Felder und Argumente:
// Jetzt werden wir einen Builder verwenden, um ein IF-Feld zu erstellen, das einen von zwei benutzerdefinierten Zeichenkettenwerten anzeigt,
// abhängig vom Wahr/Falsch‑Wert seines Ausdrucks. Um einen Wahr/Falsch‑Wert zu erhalten
// der bestimmt, welche Zeichenkette das IF-Feld anzeigt, wird das IF-Feld zwei numerische Ausdrücke auf Gleichheit prüfen.
// Wir werden die beiden Ausdrücke in Form von Formel‑Feldern bereitstellen, die wir innerhalb des IF-Feldes verschachteln.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Als Nächstes werden wir zwei Feldargumente erstellen, die als Wahr/Falsch‑Ausgabezeichenketten für das IF-Feld dienen.
// Diese Argumente werden die Ausgabewerte unserer numerischen Ausdrücke wiederverwenden.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Abschließend werden wir einen weiteren Field Builder für das IF-Feld erstellen und alle Ausdrücke kombinieren.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Siehe auch

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(const System::String\&) method


Fügt ein Argument zum Feld hinzu.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(const System::String &argument)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Argument | const System::String\& | Der Argumentwert. |

## Beispiele



Zeigt, wie Felder mit einem Field Builder erstellt und anschließend in das Dokument eingefügt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nachfolgend finden Sie drei Beispiele für die Feldkonstruktion mit einem Field Builder.
// 1 -  Einzelnes Feld:
// Verwenden Sie einen Field Builder, um ein SYMBOL-Feld hinzuzufügen, das das ƒ (Florin)-Symbol anzeigt.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Verschachteltes Feld:
// Verwenden Sie einen Field Builder, um ein Formel-Feld zu erstellen, das von einem anderen Field Builder als inneres Feld verwendet wird.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Erstellen Sie einen weiteren Builder für ein weiteres SYMBOL-Feld und fügen Sie das Formel-Feld ein
// das wir oben erstellt haben, in das SYMBOL-Feld als Argument ein.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Das äußere SYMBOL-Feld wird das Ergebnis des Formel-Feldes, 174, als Argument verwenden,
// was dazu führt, dass das Feld das ® (Registered Sign)-Symbol anzeigt, da seine Zeichen‑Nummer 174 ist.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Mehrere verschachtelte Felder und Argumente:
// Jetzt werden wir einen Builder verwenden, um ein IF-Feld zu erstellen, das einen von zwei benutzerdefinierten Zeichenkettenwerten anzeigt,
// abhängig vom Wahr/Falsch‑Wert seines Ausdrucks. Um einen Wahr/Falsch‑Wert zu erhalten
// der bestimmt, welche Zeichenkette das IF-Feld anzeigt, wird das IF-Feld zwei numerische Ausdrücke auf Gleichheit prüfen.
// Wir werden die beiden Ausdrücke in Form von Formel‑Feldern bereitstellen, die wir innerhalb des IF-Feldes verschachteln.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Als Nächstes werden wir zwei Feldargumente erstellen, die als Wahr/Falsch‑Ausgabezeichenketten für das IF-Feld dienen.
// Diese Argumente werden die Ausgabewerte unserer numerischen Ausdrücke wiederverwenden.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Abschließend werden wir einen weiteren Field Builder für das IF-Feld erstellen und alle Ausdrücke kombinieren.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Siehe auch

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(double) method


Fügt ein Argument zum Feld hinzu.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(double argument)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Argument | double | Der Argumentwert. |

## Beispiele



Zeigt, wie Felder mit einem Field Builder erstellt und anschließend in das Dokument eingefügt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nachfolgend finden Sie drei Beispiele für die Feldkonstruktion mit einem Field Builder.
// 1 -  Einzelnes Feld:
// Verwenden Sie einen Field Builder, um ein SYMBOL-Feld hinzuzufügen, das das ƒ (Florin)-Symbol anzeigt.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Verschachteltes Feld:
// Verwenden Sie einen Field Builder, um ein Formel-Feld zu erstellen, das von einem anderen Field Builder als inneres Feld verwendet wird.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Erstellen Sie einen weiteren Builder für ein weiteres SYMBOL-Feld und fügen Sie das Formel-Feld ein
// das wir oben erstellt haben, in das SYMBOL-Feld als Argument ein.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Das äußere SYMBOL-Feld wird das Ergebnis des Formel-Feldes, 174, als Argument verwenden,
// was dazu führt, dass das Feld das ® (Registered Sign)-Symbol anzeigt, da seine Zeichen‑Nummer 174 ist.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Mehrere verschachtelte Felder und Argumente:
// Jetzt werden wir einen Builder verwenden, um ein IF-Feld zu erstellen, das einen von zwei benutzerdefinierten Zeichenkettenwerten anzeigt,
// abhängig vom Wahr/Falsch‑Wert seines Ausdrucks. Um einen Wahr/Falsch‑Wert zu erhalten
// der bestimmt, welche Zeichenkette das IF-Feld anzeigt, wird das IF-Feld zwei numerische Ausdrücke auf Gleichheit prüfen.
// Wir werden die beiden Ausdrücke in Form von Formel‑Feldern bereitstellen, die wir innerhalb des IF-Feldes verschachteln.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Als Nächstes werden wir zwei Feldargumente erstellen, die als Wahr/Falsch‑Ausgabezeichenketten für das IF-Feld dienen.
// Diese Argumente werden die Ausgabewerte unserer numerischen Ausdrücke wiederverwenden.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Abschließend werden wir einen weiteren Field Builder für das IF-Feld erstellen und alle Ausdrücke kombinieren.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Siehe auch

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(int32_t) method


Fügt ein Argument zum Feld hinzu.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(int32_t argument)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Argument | int32_t | Der Argumentwert. |

## Beispiele



Zeigt, wie Felder mit einem Field Builder erstellt und anschließend in das Dokument eingefügt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nachfolgend finden Sie drei Beispiele für die Feldkonstruktion mit einem Field Builder.
// 1 -  Einzelnes Feld:
// Verwenden Sie einen Field Builder, um ein SYMBOL-Feld hinzuzufügen, das das ƒ (Florin)-Symbol anzeigt.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Verschachteltes Feld:
// Verwenden Sie einen Field Builder, um ein Formel-Feld zu erstellen, das von einem anderen Field Builder als inneres Feld verwendet wird.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Erstellen Sie einen weiteren Builder für ein weiteres SYMBOL-Feld und fügen Sie das Formel-Feld ein
// das wir oben erstellt haben, in das SYMBOL-Feld als Argument ein.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Das äußere SYMBOL-Feld wird das Ergebnis des Formel-Feldes, 174, als Argument verwenden,
// was dazu führt, dass das Feld das ® (Registered Sign)-Symbol anzeigt, da seine Zeichen‑Nummer 174 ist.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Mehrere verschachtelte Felder und Argumente:
// Jetzt werden wir einen Builder verwenden, um ein IF-Feld zu erstellen, das einen von zwei benutzerdefinierten Zeichenkettenwerten anzeigt,
// abhängig vom Wahr/Falsch‑Wert seines Ausdrucks. Um einen Wahr/Falsch‑Wert zu erhalten
// der bestimmt, welche Zeichenkette das IF-Feld anzeigt, wird das IF-Feld zwei numerische Ausdrücke auf Gleichheit prüfen.
// Wir werden die beiden Ausdrücke in Form von Formel‑Feldern bereitstellen, die wir innerhalb des IF-Feldes verschachteln.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Als Nächstes werden wir zwei Feldargumente erstellen, die als Wahr/Falsch‑Ausgabezeichenketten für das IF-Feld dienen.
// Diese Argumente werden die Ausgabewerte unserer numerischen Ausdrücke wiederverwenden.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Abschließend werden wir einen weiteren Field Builder für das IF-Feld erstellen und alle Ausdrücke kombinieren.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Siehe auch

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
