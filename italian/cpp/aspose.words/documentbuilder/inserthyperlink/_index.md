---
title: "Metodo Aspose::Words::DocumentBuilder::InsertHyperlink"
linktitle: "InsertHyperlink"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::InsertHyperlink. Inserisce un collegamento ipertestuale nel documento in C++."
type: docs
weight: 38000
url: /it/cpp/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder::InsertHyperlink method


Inserisce un collegamento ipertestuale nel documento.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertHyperlink(const System::String &displayText, const System::String &urlOrBookmark, bool isBookmark)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| displayText | const System::String\& | Testo del collegamento da visualizzare nel documento. |
| urlOrBookmark | const System::String\& | Destinazione del collegamento. Può essere un url o il nome di un segnalibro all'interno del documento. Questo metodo aggiunge sempre gli apostrofi all'inizio e alla fine dell'url. |
| isBookmark | bool | **true** se il parametro precedente è il nome di un segnalibro all'interno del documento; **false** se il parametro precedente è un URL. |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo inserito.
## Note


Nota che è necessario specificare la formattazione del carattere per il testo visualizzato del collegamento ipertestuale esplicitamente usando la proprietà [Font](../get_font/).

Questo metodo chiama internamente [InsertField()](../) per inserire un campo HYPERLINK di MS Word nel documento.

## Esempi



Mostra come inserire un campo collegamento ipertestuale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Inserisci un collegamento ipertestuale e enfatizzalo con una formattazione personalizzata.
// Il collegamento ipertestuale sarà un pezzo di testo cliccabile che ci porterà alla posizione specificata nell'URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + clic sinistro sul collegamento nel testo in Microsoft Word ci porterà all'URL tramite una nuova finestra del browser web.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


Mostra come utilizzare lo stack di formattazione di un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta la formattazione del carattere, poi scrivi il testo che precede il collegamento ipertestuale.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Conserva la nostra configurazione di formattazione corrente nello stack.
builder->PushFont();

// Modifica la formattazione corrente del builder applicando un nuovo stile.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Ripristina la formattazione del carattere che abbiamo salvato in precedenza e rimuovi l'elemento dallo stack.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```


Mostra come inserire un collegamento ipertestuale che fa riferimento a un segnalibro locale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Inserisci un campo HYPERLINK che collega al segnalibro. Possiamo passare gli switch del campo
// al metodo \"InsertHyperlink\" come parte dell'argomento contenente il nome del segnalibro di riferimento.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
