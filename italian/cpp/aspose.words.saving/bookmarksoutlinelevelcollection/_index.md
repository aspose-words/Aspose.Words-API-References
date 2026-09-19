---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection class"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection class. Una raccolta di livelli di contorno dei segnalibri individuali. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class


Una raccolta di livello di contorno dei segnalibri individuali. Per saperne di più, visita l'articolo di documentazione [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarksOutlineLevelCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, int32_t>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::String\&, int32_t) | Aggiunge un segnalibro alla raccolta. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection/)() |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [Contains](./contains/)(const System::String\&) | Determina se la raccolta contiene un segnalibro con il nome specificato. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Ottiene o imposta il livello di contorno di un segnalibro per nome. |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta il livello di contorno di un segnalibro all'indice specificato. |
| [idx_set](./idx_set/)(const System::String\&, int32_t) | Ottiene o imposta il livello di contorno di un segnalibro per nome. |
| [idx_set](./idx_set/)(int32_t, int32_t) | Ottiene o imposta il livello di contorno di un segnalibro all'indice specificato. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Restituisce l'indice basato su zero del segnalibro specificato nella raccolta. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Rimuove un segnalibro con il nome specificato dalla raccolta. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un segnalibro all'indice specificato. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descrizione |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Note


La chiave è un nome di segnalibro stringa non sensibile al maiuscolo/minuscolo. Il valore è un intero livello di contorno del segnalibro.

[Bookmark](../../aspose.words/bookmark/) outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline. Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.

## Esempi



Mostra come impostare i livelli di contorno per i segnalibri.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un segnalibro con un altro segnalibro annidato al suo interno.
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// Inserisci un altro segnalibro.
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// Durante il salvataggio in .pdf, i segnalibri possono essere accessi tramite un menu a discesa e utilizzati come ancore dalla maggior parte dei lettori.
// I segnalibri possono anche avere valori numerici per i livelli di struttura,
// consentendo alle voci di struttura di livello inferiore di nascondere le voci figlio di livello superiore quando vengono compresse nel lettore.
auto pdfSaveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> outlineLevels = pdfSaveOptions->get_OutlineOptions()->get_BookmarksOutlineLevels();

outlineLevels->Add(u"Bookmark 1", 1);
outlineLevels->Add(u"Bookmark 2", 2);
outlineLevels->Add(u"Bookmark 3", 3);

ASSERT_EQ(3, outlineLevels->get_Count());
ASSERT_TRUE(outlineLevels->Contains(u"Bookmark 1"));
ASSERT_EQ(1, outlineLevels->idx_get(0));
ASSERT_EQ(2, outlineLevels->idx_get(u"Bookmark 2"));
ASSERT_EQ(2, outlineLevels->IndexOfKey(u"Bookmark 3"));

// Possiamo rimuovere due elementi in modo che rimanga solo la designazione del livello di struttura per "Bookmark 1".
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// Ci sono nove livelli di struttura. La loro numerazione sarà ottimizzata durante l'operazione di salvataggio.
// In questo caso, i livelli "5" e "9" diventeranno "2" e "3".
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Svuotare questa raccolta conserverà i segnalibri e li posizionerà tutti sullo stesso livello di struttura.
outlineLevels->Clear();
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
