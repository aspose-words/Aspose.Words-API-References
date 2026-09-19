---
title: "Metodo Aspose::Words::Style::get_Font"
linktitle: "get_Font"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::get_Font. Ottiene la formattazione dei caratteri dello stile in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/style/get_font/
---
## Style::get_Font method


Ottiene la formattazione dei caratteri dello stile.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Style::get_Font()
```

## Note


Per gli stili di elenco questa proprietà restituisce **null**.

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

* Class [Font](../../font/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
