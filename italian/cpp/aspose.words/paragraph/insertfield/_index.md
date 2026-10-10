---
title: "Aspose::Words::Paragraph::InsertField metodo"
linktitle: "InsertField"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::InsertField metodo. Inserisce un campo in questo paragrafo in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserisce un campo in questo paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Il tipo del campo da inserire. |
| updateField | bool | Specifica se aggiornare il campo immediatamente. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Nodo di riferimento all'interno di questo paragrafo (se *refNode* è **null**, allora viene aggiunto alla fine del paragrafo). |
| isAfter | bool | Se inserire il campo dopo o prima del nodo di riferimento. |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo inserito.

## Esempi



Mostra vari modi per aggiungere campi a un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Di seguito sono riportati tre modi per inserire un campo in un paragrafo.
// 1 -  Inserisci un campo AUTHOR in un paragrafo dopo uno dei nodi figlio del paragrafo:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Inserisci un campo QUOTE dopo uno dei nodi figlio del paragrafo:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Inserisci un campo QUOTE prima di uno dei nodi figlio del paragrafo,
// e fallo visualizzare un valore segnaposto:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorniamo.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserisce un campo in questo paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | const System::String\& | Il codice campo da inserire (senza parentesi graffe). |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Nodo di riferimento all'interno di questo paragrafo (se *refNode* è **null**, allora viene aggiunto alla fine del paragrafo). |
| isAfter | bool | Se inserire il campo dopo o prima del nodo di riferimento. |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo inserito.

## Esempi



Mostra vari modi per aggiungere campi a un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Di seguito sono riportati tre modi per inserire un campo in un paragrafo.
// 1 -  Inserisci un campo AUTHOR in un paragrafo dopo uno dei nodi figlio del paragrafo:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Inserisci un campo QUOTE dopo uno dei nodi figlio del paragrafo:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Inserisci un campo QUOTE prima di uno dei nodi figlio del paragrafo,
// e fallo visualizzare un valore segnaposto:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorniamo.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserisce un campo in questo paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | const System::String\& | Il codice campo da inserire (senza parentesi graffe). |
| fieldValue | const System::String\& | Il valore del campo da inserire. Passare **null** per i campi che non hanno un valore. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Nodo di riferimento all'interno di questo paragrafo (se *refNode* è **null**, allora viene aggiunto alla fine del paragrafo). |
| isAfter | bool | Se inserire il campo dopo o prima del nodo di riferimento. |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo inserito.

## Esempi



Mostra vari modi per aggiungere campi a un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Di seguito sono riportati tre modi per inserire un campo in un paragrafo.
// 1 -  Inserisci un campo AUTHOR in un paragrafo dopo uno dei nodi figlio del paragrafo:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Inserisci un campo QUOTE dopo uno dei nodi figlio del paragrafo:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Inserisci un campo QUOTE prima di uno dei nodi figlio del paragrafo,
// e fallo visualizzare un valore segnaposto:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Questo campo visualizzerà il suo valore segnaposto finché non lo aggiorniamo.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
