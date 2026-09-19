---
title: "Classe Aspose::Words::JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::JoinRunsOptions. Fornisce flag di configurazione per l'operazione di unione delle sequenze in C++."
type: docs
weight: 38500
url: /it/cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


Fornisce flag di configurazione per l'operazione di unione delle run.

```cpp
class JoinRunsOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | Vero indica che gli attributi insignificanti di tutte le sequenze saranno ignorati durante l'unione delle sequenze con la stessa formattazione. |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | Vero indica che gli attributi ridondanti di tutte le sequenze saranno ignorati durante l'unione delle sequenze con la stessa formattazione. |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | Vero indica che gli attributi di spaziatura di tutte le sequenze saranno ignorati durante l'unione delle sequenze con la stessa formattazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | Vero indica che gli attributi insignificanti di tutte le sequenze saranno ignorati durante l'unione delle sequenze con la stessa formattazione. |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | Vero indica che gli attributi ridondanti di tutte le sequenze saranno ignorati durante l'unione delle sequenze con la stessa formattazione. |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | Vero indica che gli attributi di spaziatura di tutte le sequenze saranno ignorati durante l'unione delle sequenze con la stessa formattazione. |
| static [Type](./type/)() |  |

## Esempi



Mostra come unire le sequenze con la stessa formattazione ignorando gli attributi ridondanti e insignificanti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea sequenze con formattazione visibile identica ma con alcune differenze interne.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Verifica le sequenze prima dell'unione.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Configura le opzioni per ignorare gli attributi ridondanti e insignificanti durante l'unione.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Ignora le proprietà ridondanti delle sequenze che non influenzano l'aspetto.
options->set_IgnoreInsignificant(true);
// Ignora le differenze insignificanti come le sequenze composte solo da spazi bianchi.

// Unisci le sequenze che hanno la stessa formattazione visibile utilizzando le opzioni estese.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Verifica che le sequenze siano state unite correttamente.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
