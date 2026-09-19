---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt metodo"
linktitle: "RemoveAt"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt metodo. Rimuove un segnalibro all'indice specificato in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/removeat/
---
## BookmarksOutlineLevelCollection::RemoveAt method


Rimuove un segnalibro all'indice specificato.

```cpp
void Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | L'indice a base zero. |

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

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
