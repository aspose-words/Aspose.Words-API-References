---
title: "Aspose::Words::DocumentBuilder::EndBookmark metodo"
linktitle: "EndBookmark"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::EndBookmark metodo. Contrassegna la posizione corrente nel documento come fine segnalibro in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder::EndBookmark method


Segna la posizione corrente nel documento come fine segnalibro.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndBookmark(const System::String &bookmarkName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nome del segnalibro. |

### ReturnValue

Il nodo di fine segnalibro appena creato.
## Note


I segnalibri in un documento possono sovrapporsi e coprire qualsiasi intervallo. Per creare un segnalibro valido è necessario chiamare sia [StartBookmark()](../) sia [EndBookmark()](../) con lo stesso parametro *bookmarkName*.

I segnalibri malformati o i segnalibri con nomi duplicati verranno ignorati quando il documento viene salvato.

## Esempi



Mostra come creare un segnalibro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un segnalibro valido deve avere il testo del corpo del documento racchiuso da
// Nodi BookmarkStart e BookmarkEnd creati con un nome di segnalibro corrispondente.
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
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

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
