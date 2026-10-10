---
title: "Aspose::Words::Section::ClearHeadersFooters méthode"
linktitle: "ClearHeadersFooters"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Section::ClearHeadersFooters méthode. Efface les en-têtes et pieds de page de cette section en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters() method


Efface les en-têtes et pieds de page de cette section.

```cpp
void Aspose::Words::Section::ClearHeadersFooters()
```

## Remarques


Le texte de tous les en-têtes et pieds de page est effacé, mais les objets [HeaderFooter](../../headerfooter/) eux‑mêmes ne sont pas supprimés.

Cela rend les en-têtes et pieds de page de cette section liés aux en-têtes et pieds de page de la section précédente.

## Exemples



Montre comment effacer le contenu de tous les en-têtes et pieds de page d'une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the primary header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the primary footer.");

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(u"This is the primary header.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"This is the primary footer.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Videz tous les en-têtes et pieds de page de cette section de tout leur contenu.
// Les en-têtes et pieds de page eux‑mêmes seront toujours présents mais n'auront rien à afficher.
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
```

## Voir aussi

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Section::ClearHeadersFooters(bool) method


Efface les en-têtes et pieds de page de cette section.

```cpp
void Aspose::Words::Section::ClearHeadersFooters(bool preserveWatermarks)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| preserveWatermarks | bool | Vrai si les filigranes ne doivent pas être supprimés. |
## Remarques


Le texte de tous les en-têtes et pieds de page est effacé, mais les objets [HeaderFooter](../../headerfooter/) eux‑mêmes ne sont pas supprimés.

Cela rend les en-têtes et pieds de page de cette section liés aux en-têtes et pieds de page de la section précédente.

## Exemples



Montre comment effacer le contenu de l'en-tête et du pied de page avec ou sans filigrane.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Ajoutez un filigrane texte simple.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Assurez‑vous que les en-têtes et pieds de page contiennent du contenu.
System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"First header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"Second header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"Third header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"First footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"Second footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"Third footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Supprime tout le contenu des en-têtes et pieds de page, sauf les filigranes.
doc->get_FirstSection()->ClearHeadersFooters(true);

headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
ASSERT_EQ(Aspose::Words::WatermarkType::Text, doc->get_Watermark()->get_Type());

// Supprime tout le contenu des en-têtes et pieds de page, y compris les filigranes.
doc->get_FirstSection()->ClearHeadersFooters(false);
ASSERT_EQ(Aspose::Words::WatermarkType::None, doc->get_Watermark()->get_Type());
```

## Voir aussi

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
