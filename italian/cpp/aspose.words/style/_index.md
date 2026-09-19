---
title: "Aspose::Words::Style class"
linktitle: "Style"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Style class. Rappresenta uno stile integrato o definito dall'utente. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 64000
url: /it/cpp/aspose.words/style/
---
## Style class


Rappresenta uno stile incorporato o definito dall'utente. Per saperne di più, visita l'articolo di documentazione [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Confronta con lo stile specificato. Gli Istd degli stili sono confrontati solo per gli stili integrati. I valori predefiniti degli stili non sono inclusi nel confronto. Lo stile base, lo stile collegato e lo stile del paragrafo successivo sono confrontati ricorsivamente. |
| [get_Aliases](./get_aliases/)() | Restituisce tutti gli alias di questo stile. Se lo stile non ha alias, viene restituito un array vuoto di stringhe. |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | Specifica se questo stile è ridefinito automaticamente in base al valore appropriato. |
| [get_BaseStyleName](./get_basestylename/)() | Ottiene/Imposta il nome dello stile su cui si basa questo stile. |
| [get_BuiltIn](./get_builtin/)() | Vero se questo stile è uno degli stili integrati in MS Word. |
| [get_Document](./get_document/)() | Restituisce il documento proprietario. |
| [get_Font](./get_font/)() | Ottiene la formattazione dei caratteri dello stile. |
| [get_IsHeading](./get_isheading/)() | Vero quando lo stile è uno degli stili di intestazione integrati. |
| [get_IsQuickStyle](./get_isquickstyle/)() const | Specifica se questo stile è mostrato nella galleria rapida [Style](./) all'interno dell'interfaccia di MS Word. |
| [get_LinkedStyleName](./get_linkedstylename/)() | Ottiene/Imposta il nome dello [Style](./) collegato a questo. Restituisce una stringa vuota se non ci sono stili collegati. |
| [get_List](./get_list/)() | Ottiene l'elenco che definisce la formattazione di questo stile di elenco. |
| [get_ListFormat](./get_listformat/)() | Fornisce l'accesso alle proprietà di formattazione dell'elenco di uno stile di paragrafo. |
| [get_Locked](./get_locked/)() const | Specifica se questo stile è bloccato. |
| [get_Name](./get_name/)() const | Ottiene o imposta il nome dello stile. |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | Ottiene/Imposta il nome dello stile da applicare automaticamente a un nuovo paragrafo inserito dopo un paragrafo formattato con lo stile specificato. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Ottiene la formattazione del paragrafo dello stile. |
| [get_Priority](./get_priority/)() const | Ottiene/Imposta il valore intero che rappresenta la priorità per l'ordinamento degli stili nel riquadro attività Stili. |
| [get_SemiHidden](./get_semihidden/)() const | Ottiene/imposta se lo stile è nascosto dalla galleria Stili e dal riquadro attività Stili. |
| [get_StyleIdentifier](./get_styleidentifier/)() const | Ottiene l'identificatore di stile indipendente dalla locale per uno stile predefinito. |
| [get_Styles](./get_styles/)() const | Ottiene la raccolta di stili a cui appartiene questo stile. |
| [get_Type](./get_type/)() const | Ottiene il tipo di stile (paragrafo o carattere). |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | Ottiene/imposta se lo stile utilizzato nel documento corrente viene mostrato nella galleria Stili e nel riquadro attività Stili. True quando lo stile usato deve essere visualizzato nella galleria Stili. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Rimuove lo stile specificato dal documento. |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | Impostatore per [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/). |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | Impostatore per [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/). |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | Impostatore per [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/). |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | Impostatore per [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/). |
| [set_Locked](./set_locked/)(bool) | Impostatore per [Aspose::Words::Style::get_Locked](./get_locked/). |
| [set_Name](./set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Style::get_Name](./get_name/). |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | Impostatore per [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/). |
| [set_Priority](./set_priority/)(int32_t) | Impostatore per [Aspose::Words::Style::get_Priority](./get_priority/). |
| [set_SemiHidden](./set_semihidden/)(bool) | Impostatore per [Aspose::Words::Style::get_SemiHidden](./get_semihidden/). |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | Impostatore per [Aspose::Words::Style::get_UnhideWhenUsed](./get_unhidewhenused/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come creare e applicare uno stile personalizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Ridefinisci automaticamente lo stile.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Applica uno degli stili del documento al paragrafo che il document builder sta creando.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Rimuovi il nostro stile personalizzato dalla raccolta di stili del documento.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Qualsiasi testo che utilizzava uno stile rimosso ritorna alla formattazione predefinita.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


Mostra come creare e utilizzare uno stile di paragrafo con formattazione elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea uno stile di paragrafo personalizzato.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Crea un elenco e assicurati che i paragrafi che usano questo stile lo utilizzino.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Applica lo stile di paragrafo al paragrafo corrente del document builder, quindi aggiungi del testo.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Modifica lo stile del DocumentBuilder in uno che non abbia formattazione di elenco e scrivi un altro paragrafo.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
