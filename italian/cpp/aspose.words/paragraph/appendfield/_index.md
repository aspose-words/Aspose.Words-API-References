---
title: "Aspose::Words::Paragraph::AppendField metodo"
linktitle: "AppendField"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::AppendField metodo. Aggiunge un campo a questo paragrafo in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


Aggiunge un campo a questo paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Il tipo del campo da aggiungere. |
| updateField | bool | Specifica se aggiornare il campo immediatamente. |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo aggiunto.

## Esempi



Mostra vari modi per aggiungere campi a un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Di seguito sono riportati tre modi per aggiungere un campo alla fine di un paragrafo.
// 1 -  Aggiungi un campo DATE usando un tipo di campo, quindi aggiornalo:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Aggiungi un campo TIME usando un codice di campo:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Aggiungi un campo QUOTE usando un codice di campo, e fallo visualizzare un valore segnaposto:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorniamo.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


Aggiunge un campo a questo paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | const System::String\& | Il codice del campo da aggiungere (senza parentesi graffe). |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo aggiunto.

## Esempi



Mostra vari modi per aggiungere campi a un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Di seguito sono riportati tre modi per aggiungere un campo alla fine di un paragrafo.
// 1 -  Aggiungi un campo DATE usando un tipo di campo, quindi aggiornalo:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Aggiungi un campo TIME usando un codice di campo:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Aggiungi un campo QUOTE usando un codice di campo, e fallo visualizzare un valore segnaposto:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorniamo.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


Aggiunge un campo a questo paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | const System::String\& | Il codice del campo da aggiungere (senza parentesi graffe). |
| fieldValue | const System::String\& | Il valore del campo da aggiungere. Passa **null** per i campi che non hanno un valore. |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo aggiunto.

## Esempi



Mostra vari modi per aggiungere campi a un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Di seguito sono riportati tre modi per aggiungere un campo alla fine di un paragrafo.
// 1 -  Aggiungi un campo DATE usando un tipo di campo, quindi aggiornalo:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Aggiungi un campo TIME usando un codice di campo:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Aggiungi un campo QUOTE usando un codice di campo, e fallo visualizzare un valore segnaposto:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorniamo.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
